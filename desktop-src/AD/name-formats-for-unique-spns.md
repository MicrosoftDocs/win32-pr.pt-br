---
title: Formatos de nome para SPNs exclusivos
description: Um SPN deve ser exclusivo na floresta em que está registrado.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formatos de nome para o AD de SPNs exclusivos
- Nome da Entidade de Serviço AD , formatos de nome para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b041f88bc025c604ec5f0ad9a6bf5ba7f4cdabc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472331"
---
# <a name="name-formats-for-unique-spns"></a>Formatos de nome para SPNs exclusivos

Um SPN deve ser exclusivo na floresta em que está registrado. Se não for exclusivo, a autenticação falhará. A sintaxe spn tem quatro elementos: dois elementos necessários e dois elementos adicionais que você pode usar, se necessário, para produzir um nome exclusivo conforme listado na tabela a seguir.


```C++
<service class>/<host>:<port>/<service name>
```






| Elemento | Descrição | 
|---------|-------------|
| "<service class>" | Uma cadeia de caracteres que identifica a classe geral de serviço; por exemplo, "SqlServer". Há nomes de classe de serviço conhecidos, como "www" para um serviço Web ou "ldap" para um serviço de diretório. Em geral, essa pode ser qualquer cadeia de caracteres exclusiva da classe de serviço. Esteja ciente de que a sintaxe spn usa uma barra (/) para separar elementos, portanto, esse caractere não pode aparecer em um nome de classe de serviço. | 
| "<host>" | O nome do computador no qual o serviço está sendo executado. Pode ser um nome DNS totalmente qualificado ou um nome NetBIOS. Saiba que não há garantia de que os nomes NetBIOS serão exclusivos em uma floresta; portanto, um SPN que contém um nome NetBIOS pode não ser exclusivo. | 
| "<port>" | Um número de porta opcional para diferenciar entre várias instâncias da mesma classe de serviço em um único computador host. Omita esse componente se o serviço usar a porta padrão para sua classe de serviço. | 
| "<service name>" | Um nome opcional usado nos SPNs de um serviço replicado para identificar os dados ou serviços fornecidos pelo serviço ou pelo domínio atendido pelo serviço. Esse componente pode ter um dos seguintes formatos:<ul><li>O nome diferenciado ou objectGUID de um objeto Active Directory Domain Services, como um SCP (ponto de conexão de serviço).</li><li>O nome DNS do domínio para um serviço que fornece um serviço especificado para um domínio como um todo.</li><li>O nome DNS de um registro SRV ou MX.</li></ul> | 




 

Os componentes presentes nos SPNs de um serviço dependem de como o serviço é identificado e replicado. Há dois cenários básicos: serviços baseados em host e serviços relicáveis.

## <a name="host-based-services"></a>Serviços baseados em host

Para um serviço baseado em host, o componente " nome do serviço " é omitido porque o serviço é identificado exclusivamente pela classe de serviço e pelo nome do computador host no qual o serviço &lt; &gt; está instalado.


```C++
<service class>/<host>
```



Somente a classe de serviço é suficiente para identificar para os clientes os recursos que o serviço fornece. Você pode instalar instâncias da classe de serviço em muitos computadores e cada instância fornece serviços identificados com seu computador host. FTP e Telnet são exemplos de serviços baseados em host. Os SPNs de uma instância de serviço baseada em host poderão incluir o número da porta se o serviço usar uma porta não padrão ou houver várias instâncias do serviço no host.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Serviços relicáveis

Para um serviço relicável, pode haver uma ou várias instâncias do serviço (réplicas) e os clientes não diferenciam a qual réplica eles se conectam porque cada uma fornece o mesmo serviço. Os SPNs para cada réplica têm os mesmos componentes " classe de serviço " e " nome do serviço ", em que " nome do serviço " identifica mais especificamente os recursos &lt; &gt; &lt; &gt; &lt; &gt; fornecidos pelo serviço. Somente os componentes " &lt; host " e " porta " &gt; &lt; &gt; opcionais variariam de SPN para SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Um exemplo de um serviço relicável seria uma instância de um serviço de banco de dados que fornece acesso a um banco de dados especificado. Nesse caso, " classe de serviço " identifica o aplicativo de banco de dados e " nome do serviço &lt; " identifica o banco de dados &gt; &lt; &gt; específico. " nome do serviço " pode ser o nome diferenciado de um SCP (ponto de conexão &lt; &gt; de serviço) que contém dados de conexão para o banco de dados.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Se os clientes usarem o nome NetBIOS para compor o SPN de um serviço, cada réplica também deverá registrar um SPN contendo o nome NetBIOS.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Outro exemplo de um serviço relicável é aquele que fornece serviços para um domínio inteiro. Nesse caso, o componente " &lt; nome do serviço " é o nome DNS do domínio que está sendo &gt; atendido. Um KDC Kerberos é um exemplo desse tipo de serviço reprovável.

Esteja ciente de que, se o nome DNS de um computador for atualizado, o sistema atualizará o elemento " host " para todos os SPNs registrados para esse &lt; &gt; host na floresta.

 

 




