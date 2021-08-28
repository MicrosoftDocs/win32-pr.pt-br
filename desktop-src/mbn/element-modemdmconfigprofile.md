---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80684cdf2d47d203318afbfd7b5e6bc02de1d3dc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982739"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Perfil de configuração de DM de modem.

## <a name="element-hierarchy"></a>Hierarquia de elementos

**&lt;ModemDMConfigProfile&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
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
| <a href="element-1-adminenable.md">AdminEnable</a> | <p>Especifica se o perfil está habilitado administrativamente. Este é um novo elemento para v4.</p> | 
| <a href="element-1-adminroamcontrol.md">AdminRoamControl</a> | <p>Especifica se o perfil é controlado por roaming de forma administrativa. Este elemento é novo para v4. O valor desse elemento é um valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Este é um elemento opcional; Se nenhum valor for especificado, <strong>AllRoamAllowed</strong> será o padrão.</p> | 
| <a href="element-1-apnid.md">ApnID</a> | <p>Uma ID de APN associada a este perfil. Esse elemento é novo na V4 e é opcional.</p> | 
| <a href="element-1-context.md">Contexto</a> | <p>Especifica os parâmetros necessários para estabelecer uma conexão de dados.</p> | 
| <a href="element-1-name.md">Nome</a> | <p>O nome do perfil. Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> v1.</p> | 
| <a href="element-oemconnectionid.md">OemConnectionId</a> | <p>A ID de conexão do OEM para a configuração de DM do modem.</p> | 
| <a href="element-1-profilecreationtype.md">ProfileCreationType (em ModemDMConfigProfile)</a> | <p>Especifica como este perfil DM de modem foi criado.</p><p>Esse valor é usado para decidir se um usuário pode excluir o perfil. Os usuários só podem excluir perfis do <strong>Userprovisionados</strong> .</p> | 
| <a href="element-1-roamapplicability.md">RoamApplicability</a> | <p>Especifica que esse perfil está ativo somente quando a condição de roaming atual é a especificada. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP). O valor desse elemento deve ser um valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</p> | 
| <a href="element-1-simiccid.md">SimIccID</a> | <p>O número de Identifcation do SIM para dispositivos GSM. Para obter mais detalhes, consulte a documentação do elemento v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> .</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

Esse elemento mais externo (documento) pode não estar contido em outros elementos.

## <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



