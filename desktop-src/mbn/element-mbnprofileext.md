---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296405"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

O elemento **MBNProfileExt** é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.

Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais. Use o elemento filho [**ProfileConditionedOn**](element-profileconditionedon.md) de **MBNProfileExt** para especificar quais condições operacionais tornam um perfil específico o perfil ativo.

## <a name="element-hierarchy"></a>Hierarquia de elementos

**<MBNProfileExt>**

## <a name="syntax"></a>Syntax

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a>Chave

`?`   opcional (zero ou um)

`*`   opcional (zero ou mais)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento filho</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-adminenable.md">AdminEnable</a></td>
<td><p>Especifica se o perfil está habilitado administrativamente. Este é um novo elemento para v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Especifica se o perfil é controlado por roaming de forma administrativa. Este elemento é novo para v4. O valor desse elemento é um valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Este é um elemento opcional; Se nenhum valor for especificado, <strong>AllRoamAllowed</strong> será o padrão.</p></td>
</tr>
<tr class="odd">
<td><a href="element-apnid.md">ApnID</a></td>
<td><p>Uma ID de APN associada a este perfil. Esse elemento é novo na V4 e é opcional.</p></td>
</tr>
<tr class="even">
<td><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></td>
<td><p>Especifica se o dispositivo de banda larga móvel se conectará automaticamente a uma rede.</p>
<p>Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-connectionmode.md">ConnectionMode</a></td>
<td><p>Especifica a configuração de conexão automática a ser usada para um dispositivo de banda larga móvel.</p>
<p>Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-context.md">Contexto</a></td>
<td><p>Especifica os parâmetros necessários para estabelecer uma conexão de dados.</p></td>
</tr>
<tr class="odd">
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>Especifica uma lista de provedores de rede preferenciais durante o roaming.</p>
<p>Para obter detalhes, consulte a documentação do elemento v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-description.md">Descrição</a></td>
<td><p>Uma descrição do perfil.</p></td>
</tr>
<tr class="odd">
<td><a href="element-homeprovidername.md">HomeProviderName</a></td>
<td><p>O nome do provedor de início para o cartão SIM/dispositivo especificado. Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-iconfilepath.md">ICONFilePath</a></td>
<td><p>O caminho para o arquivo de ícone da conexão. A interface do usuário conexão do sistema operacional exibe o ícone quando uma conexão é feita usando esse perfil.</p>
<p>Para obter mais detalhes sobre como usar esse elemento, consulte a documentação v1 para <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</p></td>
</tr>
<tr class="odd">
<td><a href="element-isdefault.md">IsDefault</a></td>
<td><p>Especifica se esse perfil é o perfil padrão.</p>
<p>Para obter mais detalhes sobre esse elemento, consulte a documentação v1 para <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</p></td>
</tr>
<tr class="even">
<td><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></td>
<td><p>Especifica que este perfil é exclusivo para outros perfis do mesmo (s) conjunto (es) de perfis. Este elemento é novo para v4.</p></td>
</tr>
<tr class="odd">
<td><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></td>
<td><p>Especifica que esse perfil é um perfil de contexto PDP adicional muito duradouro. Se o valor desse elemento for <strong>true</strong>, <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> também deverá ser definido como <strong>true</strong>. Este é um novo elemento para v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></td>
<td><p>Especifica que este perfil deve ser usado somente para provisionamento. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP). Este elemento é novo para v4.</p>
<p>Se <strong>IsProvisioningProfile</strong> for true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> deverá ser false e <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> deverá ser manual.</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmsconfiguration.md">MmsConfiguration</a></td>
<td><p>Informações de configuração para MMS (serviço de mensagens de multimídia).</p>
<p>Além de definir os elementos de configuração dentro deste elemento, um perfil MMS deve ter as seguintes configurações.</p>
<ul>
<li>Seu elemento <a href="element-name.md"><strong>Name</strong></a> deve conter um nome exclusivo em todo o sistema.</li>
<li>Seu <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve ser definido como <strong>userprovisionado</strong>.</li>
<li>Seu <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve conter o ICCID do sim para o qual esse perfil se destina.</li>
<li>Seu <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> deve ser definido como <strong>manual</strong>.</li>
<li>Seu <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve conter o GUID para o grupo de finalidade de MMS.</li>
<li>Seu <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve ser definido como <strong>true</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="element-name.md">Nome</a></td>
<td><p>O nome do perfil. Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-profileconditionedon.md">ProfileConditionedOn</a></td>
<td><p>Especifica as condições que devem ser satisfeitas para que um perfil seja aplicável.</p>
<p>Este elemento é novo para v4. Ele permite que você especifique vários perfis que se aplicam em diferentes condições e para que o perfil apropriado seja usado automaticamente quando aplicável. Esse elemento é opcional. Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</p></td>
</tr>
<tr class="even">
<td><a href="element-profilecreationtype.md">ProfileCreationType (em MBNProfileExt)</a></td>
<td><p>Especifica o criador do perfil.</p>
<p>Para obter mais informações sobre esse elemento, consulte a documentação do elemento v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-purposegroups.md">PurposeGroups</a></td>
<td><p>Uma lista opcional de grupos de perfis, onde cada grupo inclui perfis usados para uma finalidade comum.</p>
<p>Este elemento é novo para v4 do esquema.</p>
<p>Um perfil pode ser listado em vários grupos.</p></td>
</tr>
<tr class="even">
<td><a href="element-simiccid.md">SimIccID</a></td>
<td><p>O número de Identifcation do SIM para dispositivos GSM. Para obter mais detalhes, consulte a documentação do elemento v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-subscriberid.md">Subscriberid</a></td>
<td><p>Identifica o identificador exclusivo do perfil.</p>
<p>Para uma rede GSM, isso deve conter a IMSI (identidade do assinante internacional móvel) do SIM e para dispositivos CDMA que ele deve conter o mínimo (número de identificação móvel) do dispositivo.</p>
<p>Para obter mais informações, consulte a documentação para o elemento <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>subscriberid</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

Esse elemento mais externo (documento) pode não estar contido em outros elementos.

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
