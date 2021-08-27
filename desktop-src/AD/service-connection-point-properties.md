---
title: Propriedades do ponto de conexão de serviço
description: Os atributos da classe serviceConnectionPoint são suficientes para a maioria dos serviços.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Propriedades do ponto de conexão de serviço
- pontos de conexão de serviço AD, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1343833d1a61e4df6dfc44238f9f094b00844f0b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473482"
---
# <a name="service-connection-point-properties"></a>Propriedades do ponto de conexão de serviço

Os atributos da classe **serviceConnectionPoint** são suficientes para a maioria dos serviços. Active Directory Domain Services não definem como os atributos são usados, portanto, os clientes do seu serviço devem ser capazes de interpretar e usar os dados em seu serviço SCPs. Os serviços que devem publicar dados adicionais sobre si mesmos podem estender o esquema de Active Directory criando uma subclasse da classe **serviceConnectionPoint** , fornecendo um nome distinto à subclasse. Para obter mais informações sobre extensões de esquema, consulte [estendendo o esquema](extending-the-schema.md).

Os atributos mais importantes de um SCP são **palavras-chave**, **serviceDNSName**, **serviceDNSNameType**, **objectclassname** e **ServiceBindingInformation**. Os aplicativos cliente pesquisam o diretório em busca de valores de **palavras-chave** para localizar o scp. Quando o SCP é encontrado, os clientes podem ler outros atributos para recuperar dados de serviço.




| Atributo | Descrição | 
|-----------|-------------|
| <strong>Palavras-chave</strong><br /> | O atributo <strong>Keywords</strong> pode conter vários valores de cadeia de caracteres que identificam seu serviço. Esse atributo é incluído no catálogo global, o que significa que os clientes em qualquer domínio de uma floresta corporativa podem pesquisar no catálogo global as palavras-chave associadas ao seu serviço. Esse atributo também é indexado, o que melhora o desempenho da consulta. O instalador que cria o SCP define os valores do atributo <strong>Keywords</strong> . Normalmente, esses valores não são modificados pelo serviço ativo.<br /> As palavras-chave exatas que você deve incluir em seu SCP dependem de como os clientes pesquisam seu serviço. As melhores palavras-chave a serem usadas são cadeias de caracteres de GUID, pois há garantia de que os GUIDs sejam exclusivos em uma floresta. Use o formato de cadeia de caracteres GUID retornado pela função <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString</strong></a> na Biblioteca RPC. Você também pode incluir nomes legíveis, se os clientes puderem usá-los para pesquisar seu serviço. As palavras-chave em um SCP devem incluir cadeias de caracteres GUID e/ou nomes que identifiquem os seguintes dados sobre seu serviço:<ul><li>Sua empresa ou organização: por exemplo, fabrikam.</li><li>O produto ou serviço: por exemplo, SQL Server. Isso permite que os aplicativos cliente encontrem SCPs para serviços desse tipo.</li><li>A versão específica do produto ou serviço, como 7,5.</li><li>Para SCPs que publicam um conjunto específico de dados ou recursos para um tipo de serviço, inclua uma cadeia de caracteres GUID ou um nome que identifique a instância específica. Por exemplo, um serviço de banco de dados pode publicar um SCP para um banco de dados específico. Nesse caso, o SCP incluiria um GUID de produto para identificar o serviço e outro GUID para identificar o banco de dados.</li></ul><br /> | 
| <strong>serviceDNSName</strong> e <strong>serviceDNSNameType</strong><br /> | Os aplicativos cliente usam os atributos <strong>serviceDNSName</strong> e <strong>serviceDNSNameType</strong> para determinar o computador host do serviço. O valor <strong>serviceDNSNameType</strong> indica o tipo de nome DNS especificado por <strong>ServiceDNSName</strong> geralmente "A" se <strong>serviceDNSName</strong> contiver um nome de host ou "SRV" se <strong>SERVICEDNSNAME</strong> contiver um nome de registro SRV.<br /> O valor de <strong>serviceDNSName</strong> normalmente é o nome DNS do computador host do serviço. O instalador do serviço pode chamar a função <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx devia</strong></a> para obter o nome DNS do computador local.<br /> Para serviços que têm registros SRV do DNS, <strong>serviceDNSName</strong> pode ser o nome do registro SRV. Um aplicativo cliente usa as APIs do DNS para recuperar todos os registros SRV que correspondem a esse nome. Em seguida, o cliente recupera o nome do host DNS de um dos registros SRV. Essa técnica é útil para serviços replicados porque os registros SRV também incluem dados que permitem que o cliente selecione a melhor réplica.<br /> | 
| <strong>serviceBindingInformation</strong><br /> | Uma propriedade com vários valores que contém valores de cadeia de caracteres que armazenam dados necessários para associar a um serviço. Essa propriedade é indexada e replicada para o catálogo global.<br /> O conteúdo de <strong>ServiceBindingInformation</strong> é específico para o serviço que publicou o SCP; Os clientes devem interpretar os dados de associação. No caso mais comum, os dados de associação consistem em um número de porta no computador host de serviço.<br /> | 
| <strong>serviceClassName</strong><br /> | Uma propriedade de valor único que identifica a classe de serviço representada pelo SCP. Esta é uma cadeia de caracteres descritiva específica para o serviço que publicou o SCP; por exemplo, SqlServer. Para serviços que dão suporte à autenticação mútua, os clientes podem usar essa propriedade, juntamente com o nome DNS do computador host do serviço, para formar um nome da entidade de serviço. Para obter mais informações, consulte <a href="mutual-authentication-using-kerberos.md">autenticação mútua usando o Kerberos</a>.<br /> | 




 

 

