---
description: Indica um impacto alto, médio ou baixo de um dispositivo que executa um sistema operacional desatualizado.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Enumeração UpdateImpactLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749432"
---
# <a name="updateimpactlevel-enumeration"></a>Enumeração UpdateImpactLevel

Indica um impacto alto, médio ou baixo de um dispositivo que executa um sistema operacional desatualizado. Essa enumeração é geralmente usada por estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , que, por sua vez, são aninhadas dentro do [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) retornado de [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).

## <a name="syntax"></a>Syntax


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Nenhum**
</dt> <dd>

Não há nenhum impacto previsto em seu dispositivo. Isso pode ocorrer porque o dispositivo está atualizado ou não está atualizado porque o dispositivo está respeitando sua Windows Update para períodos de adiamento de negócios ou está desatualizado, mas ainda não atingiu o limite de **daysOutOfDate** para alcançar um nível de impacto mais alto.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ baixo**
</dt> <dd>

O dispositivo não está executando o sistema operacional mais recente, mas tem uma atualização recente.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Média**
</dt> <dd>

O dispositivo está executando o sistema operacional mais recente, mas tem uma atualização moderadamente recente.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ alto**
</dt> <dd>

O dispositivo está desatualizado há muito tempo. Este dispositivo pode ter vulnerabilidades de segurança e pode estar sem correções importantes que tornam o Windows mais bem executado. Quando um dispositivo estiver executando uma versão do Windows que não tem mais suporte, o **UpdateImpactLevel \_ High** será sempre retornado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) é chamado, uma estrutura [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) é retornada. Na estrutura, há um **assessmentForCurrent** e um **assessmentForUpToDate**. Ambas são estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) . Ambos os membros têm uma enumeração **UpdateImpactLevel** , que indica um alto, médio, baixo ou nenhum impacto para um dispositivo que esteja executando um sistema operacional desatualizado. Esses níveis são determinados pelo valor de **daysOutOfDate**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                   |
| INSERI<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




