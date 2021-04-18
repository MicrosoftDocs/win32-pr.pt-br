---
title: Classe Win32_WinSAT
description: Define informações de avaliação de resumo para a avaliação formal mais recente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- WinSAT de classe de Win32_WinSAT
- Classe Win32_WinSAT WinSAT, descrita
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762996"
---
# <a name="win32_winsat-class"></a>\_Classe Win32 WinSAT

\[**Win32 \_ O WinSAT** pode ser alterado ou indisponível para versões após a Windows 8.1.\]

Define informações de avaliação de resumo para a avaliação formal mais recente.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ WinSAT** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ WinSAT** tem essas propriedades.

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma pontuação para os processadores no computador.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Depois de Windows 8.1, o WinSAT não avalia mais os recursos de gráficos tridimensionais (jogos) do computador e a capacidade do driver gráfico de processar objetos e executar sombreadores usando essa avaliação. Para compatibilidade, os valores de sentinela de relatório do WinSAT para as métricas e pontuações, no entanto, não são calculados em tempo real.

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma pontuação para a taxa de transferência de leitura sequencial no disco rígido primário no computador.

</dd> <dt>

**GraphicsScore**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma pontuação para os recursos gráficos do computador.

</dd> <dt>

**MemoryScore**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma pontuação para a taxa de transferência de memória e a capacidade do computador.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Essa propriedade deve ser definida como "MostRecentAssessment" na cláusula WHERE da consulta WQL.

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado da avaliação. Para obter uma descrição dos valores possíveis, consulte a enumeração do [**\_ \_ estado de avaliação do WINSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Válido** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Inválido** (4)
</dt> </dl>

</dd> <dt>

**WinSPRLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Pontuação básica do computador. Para obter detalhes sobre o valor de pontuação, consulte a propriedade [**IProvideWinSATResultsInfo:: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter informações sobre as pontuações do subcomponente, como **MemoryScore**, consulte a propriedade [**IProvideWinSATAssessmentInfo:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="examples"></a>Exemplos

Para obter um exemplo que mostra como usar o WMI para recuperar dados dessa classe, consulte o método [**\_ bitmap IProvideWinSATVisuals:: Get**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





