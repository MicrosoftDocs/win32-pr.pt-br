---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c47dd7c8b8064d7c9bed24763dfe3ec8fda0ac12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472122"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

O **elemento MBNProfileExt** é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de Banda Larga Móvel com um conjunto mais avançado de opções do que o elemento MBNProfile.

Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um conjunto específico de condições operacionais. Use o [**elemento filho ProfileConditionedOn**](element-profileconditionedon.md) **de MBNProfileExt** para especificar quais condições operacionais fazem de um perfil específico o perfil ativo.

## <a name="element-hierarchy"></a>Hierarquia de elementos

**<MBNProfileExt>**

## <a name="syntax"></a>Sintaxe

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


| Elemento filho | Descrição | 
|---------------|-------------|
| <a href="element-adminenable.md">AdminEnable</a> | <p>Especifica se o perfil está habilitado administrativamente. Esse é um novo elemento para v4.</p> | 
| <a href="element-adminroamcontrol.md">AdminRoamControl</a> | <p>Especifica se o perfil é controlado por roam-in administrativo. Esse elemento é novo para v4. O valor desse elemento é um <a href="simpletype-roamcontroltype.md"><strong>valor roamControlType.</strong></a> Este é um elemento opcional; se nenhum valor for especificado, <strong>AllRoamAllowed</strong> será o padrão.</p> | 
| <a href="element-apnid.md">ApnID</a> | <p>Uma ID de APN associada a esse perfil. Esse elemento é novo na v4 e é opcional.</p> | 
| <a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a> | <p>Especifica se o dispositivo de Banda Larga Móvel se conectará automaticamente a uma rede.</p><p>Para obter mais informações, consulte a documentação do <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>elemento AutoConnectOnInternet</strong></a> v1.</p> | 
| <a href="element-connectionmode.md">ConnectionMode</a> | <p>Especifica a configuração de conexão automática a ser usada para um dispositivo de banda larga móvel.</p><p>Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</p> | 
| <a href="element-context.md">Contexto</a> | <p>Especifica os parâmetros necessários para estabelecer uma conexão de dados.</p> | 
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>Especifica uma lista de provedores de rede preferenciais ao roaming.</p><p>Para obter detalhes, consulte a documentação do <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>elemento DataRoamingPartners</strong></a> v1.</p> | 
| <a href="element-description.md">Descrição</a> | <p>Uma descrição do perfil.</p> | 
| <a href="element-homeprovidername.md">HomeProviderName</a> | <p>O nome do provedor de residência para o SIM/Dispositivo determinado. Para obter mais informações, consulte a documentação do <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>elemento HomeProviderName</strong></a> v1.</p> | 
| <a href="element-iconfilepath.md">ICONFilePath</a> | <p>O caminho para o arquivo de ícone para a conexão. A interface do usuário de conexão do sistema operacional exibe o ícone quando uma conexão é feita usando esse perfil.</p><p>Para obter mais detalhes sobre como usar esse elemento, consulte a documentação da v1 <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>para ICONFilePath.</strong></a></p> | 
| <a href="element-isdefault.md">IsDefault</a> | <p>Especifica se esse perfil é o perfil padrão.</p><p>Para obter mais detalhes sobre esse elemento, consulte a documentação da v1 <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>para IsDefault.</strong></a></p> | 
| <a href="element-isexclusivetoother.md">IsExclusiveToOther</a> | <p>Especifica que esse perfil é exclusivo para outros perfis do mesmo conjunto de perfis. Esse elemento é novo para v4.</p> | 
| <a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a> | <p>Especifica que esse perfil é um perfil de contexto PDP adicional de longa duração. Se o valor desse elemento for <strong>true,</strong> <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> também deverá ser definido como <strong>true.</strong> Esse é um novo elemento para v4.</p> | 
| <a href="element-isprovisioningprofile.md">IsProvisioningProfile</a> | <p>Especifica que esse perfil deve ser usado somente para provisionamento. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto PDP (Protocolo de Dados de Pacote). Esse elemento é novo para v4.</p><p>Se <strong>IsProvisioningProfile</strong> for true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> deverá ser false e <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> deverá ser manual.</p> | 
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Informações de configuração do MMS (Serviço de Mensagens Multimídia).</p><p>Além de definir os elementos de configuração dentro desse elemento, um perfil MMS deve ter as seguintes configurações.</p><ul><li>Seu <a href="element-name.md"><strong>elemento Name</strong></a> deve conter um nome exclusivo em todo o sistema.</li><li>Seu <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve ser definido como <strong>UserProvisioned.</strong></li><li>Seu <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve conter o ICCID do SIM para o que esse perfil se destina.</li><li>Seu <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> deve ser definido como <strong>Manual.</strong></li><li>Seu <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve conter o GUID para o grupo de finalidade MMS.</li><li>Seu <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve ser definido como <strong>true.</strong></li></ul> | 
| <a href="element-name.md">Nome</a> | <p>O nome do perfil. Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> v1.</p> | 
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Especifica as condições que devem ser atendidas para que um perfil seja aplicável.</p><p>Esse elemento é novo para v4. Ele permite que você especifique vários perfis que se aplicam em condições diferentes e que o perfil adequado seja usado automaticamente quando aplicável. Esse elemento é opcional. Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</p> | 
| <a href="element-profilecreationtype.md">ProfileCreationType (em MBNProfileExt)</a> | <p>Especifica o criador do perfil.</p><p>Para obter mais informações sobre esse elemento, consulte a documentação do elemento <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> v1.</p> | 
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>Uma lista opcional de grupos de perfis, em que cada grupo inclui perfis usados para uma finalidade comum.</p><p>Esse elemento é novo para v4 do esquema.</p><p>Um perfil pode ser listado em vários grupos.</p> | 
| <a href="element-simiccid.md">SimIccID</a> | <p>O número de identificação do SIM para dispositivos GSM. Para obter mais detalhes, consulte a documentação do <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>elemento SimIccID</strong></a> v1.</p> | 
| <a href="element-subscriberid.md">SubscriberID</a> | <p>Identifica o identificador exclusivo do perfil.</p><p>Para uma rede GSM, isso deve conter o IMSI (Identidade do Assinante Móvel Internacional) do SIM e, para dispositivos CDMA, ele deve conter o MIN (Número de Identificação Móvel) do dispositivo.</p><p>Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>v1 SubscriberID.</strong></a></p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

Esse elemento mais externo (documento) pode não estar contido por outros elementos.

## <a name="requirements"></a>Requisitos


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
