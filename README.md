### Bookshop
---

https://github.com/worlduniting/bookshop
```
gem install bookshop
bookshop new my_new_book
```
```
<p>Today is <%= time.now.strftime('%A') %>.</p>
<%= import('a_whole_chapter.html.erb') %>
<%= import('bodymatter/ch01/my)first_section.html.erb') %>
# book/book.html.erb
<%= import('bodymatter/ch01/ch01.html.erb') %>
# bodymatter/ch01/ch01.html.erb
<%= import('bodymatter/ch01/first_section.html.erb') %>
<%= import('bodymatter/ch01/second_section.html.erb') %>

<% if @output == :pdf %>
<p>...</p>
<% end %>
```
```
# book.yml
isbn: 123456789010
html: 
  title: text
pdf:
  title: ...
  pub_date: 12/14/2018
epub:
  title: ...
  pub_date: 11/14/2018
```
```
<p>...<%= @book.isbn %></p>
<p>...<%= @book.html.title %></p>
<p>...<%= @book.epub.pub_date %></p>
```
```
my:
  madeup:
    friend:
      name: tky
```
```
<p>...<%= @book.my.madeup.frined.name %></p>
```
```
<p>...<%= @book.isbn %></p>
<p>Title:
  <% if @output == :html %>
    <%= @book.html.title %>
  <% elsif @output == :pdf %>
    <%= @book.pdf.title %>
  <% elsif @output == :epub %>
    <%= @book.epub.title %>
  <% end %>
</p>
```
```
bookshop build html
bookshop build pdf
bookshop build epub
bookshop new name_of_book
```
