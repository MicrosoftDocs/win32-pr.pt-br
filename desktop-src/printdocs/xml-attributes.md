---
description: Saiba mais sobre atributos XML na Estrutura de Esquema de Impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548814"
---
# <a name="xml-attributes"></a>Atributos XML

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Há vários atributos XML que aparecem em vários tipos de elemento definidos na Estrutura de Esquema de Impressão. Atributos XML com o mesmo nome geralmente têm o mesmo significado e obedecem às mesmas regras, independentemente do tipo de elemento em que residem. Portanto, os atributos XML são listados aqui por nome e não pelo tipo de elemento host. Atributos XML definidos de forma privada não são permitidos. Somente os atributos XML definidos aqui podem ser usados em um documento PrintCapabilities ou em um PrintTicket e, em seguida, somente no contexto definido.

Embora as partes privadas não tenham permissão para introduzir novas definições no namespace de outra parte, elas têm permissão para utilizar nomes existentes de outro namespace privado, desde que seu uso seja consistente com o uso estabelecido por outra parte. Portanto, uma Opção pode conter elementos ScoredProperty definidos por várias partes diferentes, cada uma residindo em namespaces diferentes.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome do atributo</th>
<th>Tipos e valores de dados</th>
<th>Finalidade</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name <br/></td>
<td>XML QName<br/></td>
<td>Esse atributo XML identifica a instância do elemento. Ele distingue um elemento de outro do mesmo tipo de elemento. Esse atributo XML é tão amplamente usado que é chamado de atributo name.<br/></td>
<td>As restrições a seguir pertencem ao atributo name.<br/>
<ul>
<li>O atributo name deve estar na forma de um QName definido por XML válido. Ou seja, ele deve ser qualificado por um namespace XML válido. Os QNames que aparecem como valores de atributos de nome devem ser explicitamente qualificados por namespace, mesmo que um namespace padrão seja definido. <br/></li>
<li>O conteúdo do caractere deve ser o de um QName definido por XML válido. <br/></li>
<li>Nomes definidos de forma privada devem ser qualificados com um namespace associado exclusivamente à parte que introduziu o atributo name.<br/></li>
<li>Requisito de exclusividade de irmão: dois elementos irmãos que pertencem ao mesmo tipo de elemento podem ter o mesmo atributo de nome. A única exceção são elementos Option, em que o atributo name pode ser usado para definir uma Opção. Portanto, os elementos Option de vários irmãos podem ter o mesmo atributo de nome.<br/></li>
<li>Os seguintes tipos de elemento podem conter atributos de nome: Property, ScoredProperty, ParameterDef, Option e Feature.<br/></li>
<li>Atributos de nome são necessários para aparecer em cada um dos tipos de elemento que os contêm, exceto no caso de alguns elementos de Opção de Esquema de Impressão público definidos anteriormente, como DocumentNUp.<br/></li>
</ul>
O exemplo a seguir mostra como identificar uma instância option usando um atributo 'name'. Essa é a maneira correta de definir elementos Option. Um provedor não deve ter opções sem nome, a menos que elas sejam definidas publicamente no Esquema de Impressão, como DocumentNUp.<br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td>Propagar <br/></td>
<td>Enumeração<br/> Nenhum valor está definido no momento.<br/></td>
<td>O atributo propagar não é usado na versão inicial do Print Schema Framework. Ele está documentado aqui para que o código de validação PrintCapabilities ou PrintTicket implementado para a versão inicial do Print Schema Framework possa processar qualquer versão de esquema subsequente sem erro.<br/></td>

</tr>
<tr class="odd">
<td>Restrita <br/></td>
<td>Enumeração<br/> Valores permitidos:<br/>
<ul>
<li>Nenhum <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>Indica se a Opção está disponível para seleção ou para uso. <br/></td>
<td>Os valores permitidos do atributo restrito têm os seguintes significados. Observe que esses valores são listados em ordem, do menos restritivo (Nenhum) ao mais restritivo (DeviceSettings).<br/> Nenhum <br/>
<ul>
<li>A Opção não está restrita. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>A opção é restrita pelas configurações printTicket. Isso implica que alterar a configuração pode remover a restrição. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>A opção é restrita pelas configurações do administrador; A opção não pode ser habilitada pelo usuário.<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>A opção é restrita pelas configurações do dispositivo ou pelas opções de dispositivo instaladas fisicamente; A Opção não pode ser habilitada pelo usuário ou pelo administrador.<br/></li>
</ul>
Quando o provedor PrintCapabilities relata valores do atributo restrito, a restrição mais restritiva encontrada deve ser relatada. Por exemplo, se uma Opção for restrita por uma configuração de administrador e uma configuração de dispositivo, o provedor PrintCapabilities deverá relatar DeviceSettings.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Esse atributo XML estabelece um vínculo entre um URI (Uniform Resource Identifier) do namespace e o prefixo de namespace que aparece no QName XML. Você deve estabelecer esse link para o URI de namespace definido para a Estrutura de Esquema de Impressão antes de usar qualquer uma das marcas de elemento definidas pelo Framework, Atributos, atributos de nome e assim por diante. Você pode declarar esse namespace como o padrão para evitar realmente qualificar as marcas de elemento com um prefixo de namespace, embora todos os outros QNames devem ser explicitamente qualificados. O namespace padrão deve ser definido no elemento raiz apropriado. Observe todas as regras XML e convenções sobre o uso do atributo xmlns.<br/> O URI da Estrutura de Esquema de Impressão é http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> O URI das palavras-chave de esquema de impressão é https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




