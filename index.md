# ⚡ Technical Ops: SysAdmin & Security
Bienvenido a mi bitácora personal. Aquí documento soluciones prácticas sobre **Administración de Sistemas**, **Arquitectura de Red** y **Hacking Ético**.

---

## 📝 Artículos Recientes

<ul>
  {% for post in paginator.posts %}
    <li>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p style="color: gray; font-size: 0.9em;">{{ post.date | date: "%d/%m/%Y" }}</p>
      <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </li>
  {% endfor %}
</ul>

{% if paginator.total_pages > 1 %}
<div style="text-align: center; margin-top: 20px;">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | relative_url }}">« Anterior</a>
  {% endif %}
  
  <span style="margin: 0 10px;">Página {{ paginator.page }} de {{ paginator.total_pages }}</span>
  
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | relative_url }}">Siguiente »</a>
  {% endif %}
</div>
{% endif %}

---
*Alejandro Ramos Naveros | [LinkedIn](https://www.linkedin.com/in/alex-arn/)*
