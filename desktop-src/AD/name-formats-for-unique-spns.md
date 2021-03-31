---
title: Formatos de nome para SPNs exclusivos
description: Um SPN deve ser exclusivo na floresta em que está registrado.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formatos de nome para anúncio de SPNs exclusivos
- ANÚNCIO do nome da entidade de serviço, formatos de nome para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159310"
---
# <a name="name-formats-for-unique-spns"></a>Formatos de nome para SPNs exclusivos

Um SPN deve ser exclusivo na floresta em que está registrado. Se não for exclusivo, haverá falha na autenticação. A sintaxe de SPN tem quatro elementos: dois elementos necessários e dois elementos adicionais que você pode usar, se necessário, para produzir um nome exclusivo, conforme listado na tabela a seguir.


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;&lt;classe de serviço&gt;&quot;</td>
<td>Uma cadeia de caracteres que identifica a classe geral do serviço; por exemplo, &quot; SqlServer &quot; . Há nomes de classe de serviço bem conhecidos, como &quot; www &quot; para um serviço Web ou &quot; LDAP &quot; para um serviço de diretório. Em geral, isso pode ser qualquer cadeia de caracteres que seja exclusiva para a classe de serviço. Lembre-se de que a sintaxe SPN usa uma barra (/) para separar elementos, portanto, esse caractere não pode aparecer em um nome de classe de serviço.</td>
</tr>
<tr class="even">
<td>&quot;&lt;hospedeira&gt;&quot;</td>
<td>O nome do computador no qual o serviço está em execução. Pode ser um nome DNS totalmente qualificado ou um nome NetBIOS. Saiba que não há garantia de que os nomes NetBIOS serão exclusivos em uma floresta; portanto, um SPN que contém um nome NetBIOS pode não ser exclusivo.</td>
</tr>
<tr class="odd">
<td>&quot;&lt;porta&gt;&quot;</td>
<td>Um número de porta opcional para diferenciar entre várias instâncias da mesma classe de serviço em um único computador host. Omita esse componente se o serviço usar a porta padrão para sua classe de serviço.</td>
</tr>
<tr class="even">
<td>&quot;&lt;nome do serviço&gt;&quot;</td>
<td>Um nome opcional usado nos SPNs de um serviço replicável para identificar os dados ou serviços fornecidos pelo serviço ou pelo domínio servido pelo serviço. Este componente pode ter um dos seguintes formatos:
<ul>
<li>O nome distinto ou objectGUID de um objeto em Active Directory Domain Services, como um SCP (ponto de conexão de serviço).</li>
<li>O nome DNS do domínio para um serviço que fornece um serviço especificado para um domínio como um todo.</li>
<li>O nome DNS de um registro SRV ou MX.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Os componentes presentes nos SPNs de um serviço dependem de como o serviço é identificado e replicado. Há dois cenários básicos: serviços baseados em host e serviços replicáveis.

## <a name="host-based-services"></a>Serviços baseados em host

Para um serviço baseado em host, o &lt; componente "nome &gt; do serviço" é omitido porque o serviço é identificado exclusivamente pela classe de serviço e o nome do computador host no qual o serviço está instalado.


```C++
<service class>/<host>
```



A classe de serviço sozinha é suficiente para identificar para clientes os recursos que o serviço fornece. Você pode instalar instâncias da classe de serviço em vários computadores e cada instância fornece serviços que são identificados com seu computador host. FTP e Telnet são exemplos de serviços baseados em host. Os SPNs de uma instância de serviço baseada em host podem incluir o número da porta se o serviço usar uma porta não padrão ou se houver várias instâncias do serviço no host.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Serviços replicáveis

Para um serviço replicável pode haver uma ou mais instâncias do serviço (réplicas), e os clientes não diferenciam a qual réplica eles se conectam porque cada uma fornece o mesmo serviço. Os SPNs de cada réplica têm os mesmos componentes de " &lt; classe &gt; de serviço" e " &lt; nome do serviço &gt; ", em que " &lt; nome &gt; do serviço" identifica mais especificamente os recursos fornecidos pelo serviço. Somente os &lt; componentes "host &gt; " e " &lt; porta" opcional &gt; variam de SPN para SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Um exemplo de um serviço replicável seria uma instância de um serviço de banco de dados que fornece acesso a um banco de dados especificado. Nesse caso, " &lt; classe de serviço &gt; " identifica o aplicativo de banco de dados e " &lt; nome &gt; do serviço" identifica o banco de dados específico. " &lt; nome &gt; do serviço" pode ser o nome distinto de um SCP (ponto de conexão de serviço) que contém dados de conexão para o banco de dado.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Se os clientes usarem o nome NetBIOS para compor o SPN de um serviço, cada réplica também deverá registrar um SPN que contenha o nome NetBIOS.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Outro exemplo de um serviço replicável é aquele que fornece serviços a um domínio inteiro. Nesse caso, o componente " &lt; nome do serviço &gt; " é o nome DNS do domínio que está sendo servido. Um KDC Kerberos é um exemplo desse tipo de serviço replicável.

Lembre-se de que, se o nome DNS de um computador for alterado, o sistema atualizará o &lt; elemento "host &gt; " para todos os SPNs registrados para esse host na floresta.

 

 




