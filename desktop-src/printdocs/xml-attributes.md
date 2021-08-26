---
description: Saiba mais sobre atributos XML na estrutura de esquema de impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Atributos XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5312137328de0bf5c2fa8609b53cdf39b7eb15fde9dc1517ae6cc0394d8c12f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886286"
---
# <a name="xml-attributes"></a>Atributos XML

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Há um número de atributos XML que aparecem em vários tipos de elementos definidos na estrutura de esquema de impressão. Os atributos XML com o mesmo nome geralmente têm o mesmo significado e obedecem às mesmas regras, independentemente do tipo de elemento no qual residem. Portanto, os atributos XML são listados aqui pelo nome e não pelo tipo de elemento host. Atributos XML definidos de modo privado não são permitidos. Somente os atributos XML definidos aqui podem ser usados em um documento de PrintCapabilities ou um PrintTicket e, em seguida, somente no contexto definido.

Embora as partes privadas não tenham permissão para introduzir novas definições no namespace de outra parte, elas são permitidas a utilizar nomes existentes de outro namespace privado, contanto que seu uso seja consistente com o uso estabelecido pela outra entidade. Portanto, uma opção pode conter elementos ScoredProperty definidos por várias partes diferentes, cada um que reside em namespaces diferentes.



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
<th>Tipos de dados e valores</th>
<th>Finalidade</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name <br/></td>
<td>QName de XML<br/></td>
<td>Esse atributo XML identifica a instância do elemento. Ele distingue um elemento de outro tipo de elemento. Esse atributo XML é muito usado e é chamado de atributo de nome.<br/></td>
<td>As restrições a seguir pertencem ao atributo de nome.<br/>
<ul>
<li>O atributo de nome deve estar na forma de um QName definido por XML válido. Ou seja, ele deve ser qualificado por um namespace XML válido. Os QNames que aparecem como valores de atributos de nome devem ser qualificados explicitamente para namespace, mesmo que um namespace padrão seja definido. <br/></li>
<li>O conteúdo do caractere deve ser de um QName definido pelo XML válido. <br/></li>
<li>Nomes definidos de forma privada devem ser qualificados com um namespace que esteja associado exclusivamente à entidade que introduziu o atributo de nome.<br/></li>
<li>Requisito de exclusividade de irmãos: não dois elementos irmãos que pertencem ao mesmo tipo de elemento podem ter o mesmo atributo de nome. A única exceção são os elementos Option, em que o atributo Name pode ser usado para definir uma opção. Portanto, elementos de opção de múltiplos irmãos podem ter o mesmo atributo de nome.<br/></li>
<li>Os seguintes tipos de elemento podem conter atributos de nome: Property, ScoredProperty, ParameterDef, Option e Feature.<br/></li>
<li>atributos de nome são necessários para aparecer em cada um dos tipos de elemento que os contêm, exceto no caso de alguns elementos de opção de esquema de impressão pública definidos anteriormente, como DocumentNUp.<br/></li>
</ul>
O exemplo a seguir mostra como identificar uma instância de opção usando um atributo ' name '. Essa é a maneira correta de definir elementos de opção. Um provedor não deve ter opções não nomeadas, a menos que elas estejam publicamente definidas no esquema de impressão, como DocumentNUp.<br/>
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
<td>propagar <br/></td>
<td>Enumeração<br/> Nenhum valor está definido no momento.<br/></td>
<td>O atributo propagar não é usado na versão inicial da estrutura de esquema de impressão. Ele está documentado aqui para que o código de validação de PrintCapabilities ou PrintTicket implementado para a versão inicial da estrutura de esquema de impressão possa processar quaisquer versões de esquema subsequentes sem erros.<br/></td>

</tr>
<tr class="odd">
<td>restrita <br/></td>
<td>Enumeração<br/> Valores permitidos:<br/>
<ul>
<li>Nenhum <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>Indica se a opção está disponível para seleção ou para uso. <br/></td>
<td>Os valores permitidos do atributo restrito têm os seguintes significados. Observe que esses valores são listados em ordem, do menos restritivo (nenhum) para o mais restritivo (DeviceSettings).<br/> Nenhum <br/>
<ul>
<li>A opção não é restrita. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>A opção é restrita pelas configurações do PrintTicket. Isso implica que a alteração da configuração pode remover a restrição. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>A opção é restrita pelas configurações do administrador; a opção não pode ser habilitada pelo usuário.<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>A opção é restrita pelas configurações do dispositivo ou pelas opções de dispositivo fisicamente instaladas; a opção não pode ser habilitada pelo usuário ou pelo administrador.<br/></li>
</ul>
Quando o provedor de PrintCapabilities relata valores do atributo restrito, a restrição mais restritiva encontrada deve ser relatada. Por exemplo, se uma opção for restrita por uma configuração de administrador e uma configuração de dispositivo, o provedor de PrintCapabilities deverá relatar DeviceSettings.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Esse atributo XML estabelece um vínculo entre um URI (Uniform Resource Identifier) de namespace e o prefixo de namespace que aparece no QName de XML. Você deve estabelecer um link desse tipo para o URI do namespace definido para a estrutura de esquema de impressão antes de poder usar qualquer uma das marcas, atributos, atributos de nome do elemento definido pelo Framework e assim por diante. Você pode declarar esse namespace como padrão para evitar realmente qualificar as marcas de elemento com um prefixo de namespace, embora todos os outros QNames devam ser explicitamente qualificados. O namespace padrão deve ser definido no elemento raiz apropriado. Observe todas as regras e convenções XML referentes ao uso do atributo xmlns.<br/> O URI para a estrutura de esquema de impressão é http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> O URI para as palavras-chave do esquema de impressão é https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




