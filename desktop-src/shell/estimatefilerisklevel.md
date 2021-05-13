---
description: Estima o risco de executar um código desconhecido quando um manipulador é chamado em um determinado arquivo. Esse risco se baseia em uma compreensão do manipulador e do conteúdo do código do arquivo.
title: Função EstimateFileRiskLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841427"
---
# <a name="estimatefilerisklevel-function"></a>Função EstimateFileRiskLevel

\[Essa função está disponível no Windows XP com Service Pack 2 (SP2) por meio do Windows Vista. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows. Em vez disso, os aplicativos cliente devem usar o [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) para apresentar um ambiente de usuário que fornece download seguro e troca de arquivos por email e anexos de mensagens.\]

Estima o risco de executar um código desconhecido quando um manipulador é chamado em um determinado arquivo. Esse risco se baseia em uma compreensão do manipulador e do conteúdo do código do arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszFilePath* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho do arquivo que está sendo verificado em relação ao manipulador.

</dd> <dt>

*pszExt* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém a extensão do arquivo que está sendo verificado, seja com ou sem seu ponto principal. Por exemplo, ". txt" ou "txt".

</dd> <dt>

*pszHandler* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho do manipulador para o arquivo.

</dd> <dt>

*pfrlEstimate* \[ fora\]
</dt> <dd>

Tipo: **FILE \_ RISK \_ LEVEL \***

Quando essa função retorna com êxito, contém um ponteiro para um dos valores a seguir que afirmam o risco estimado.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ NENHUMA \_ OPINIÃO** (0)


</dt> <dd>

O formato do arquivo não é identificado ou o manipulador não é identificado. Informações insuficientes disponíveis para uma resposta significativa.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)


</dt> <dd>

O formato do arquivo é completamente compreendido, o manipulador é conhecido e há alta confiança de que nenhum código não será executado.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERADO** (2)


</dt> <dd>

O formato do arquivo é identificado, mas não é suficientemente compreendido para rotular como um risco alto ou baixo.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ALTO** (3)


</dt> <dd>

O formato do arquivo é compreendido e fatores de risco elevados foram identificados.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)


</dt> <dd>

O formato de arquivo é bloqueado especificamente para esse manipulador.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem-sucedida, ela **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Essa função não é declarada em um header público nem incluída em um arquivo de biblioteca. Para usá-lo, você deve carregá-lo diretamente Winshfhc.dll pelo ordinal 101.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com aplicativos da \[ área de trabalho SP2\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (versão 5,1 ou posterior)</dt> </dl> |



 

 




