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
ms.openlocfilehash: 96798e0bc64b39ae7f18d58b97fafafc9dc2508b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968134"
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

Tipo: **\_ \_ nível \* de risco do arquivo* _

Quando essa função retorna com êxito, contém um ponteiro para um dos valores a seguir que estado o risco estimado.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL \_ nenhuma \_ opinião** (0)


</dt> <dd>

O formato do arquivo não é identificado ou o manipulador não foi identificado. Informações insuficientes disponíveis para uma resposta significativa.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ BAIXO** (1)


</dt> <dd>

O formato do arquivo é completamente compreendido, o manipulador é conhecido e há alta confiança de que nenhum código estranho será executado.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERADO** (2)


</dt> <dd>

O formato do arquivo é identificado, mas não é suficientemente compreendido para o rótulo como um risco alto ou baixo.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ALTA** (3)


</dt> <dd>

O formato de arquivo é compreendido e os fatores de risco elevado foram identificados.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCO** (4)


</dt> <dd>

O formato de arquivo é especificamente bloqueado para este manipulador.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função não é declarada em um cabeçalho público ou está incluída em um arquivo de biblioteca. Para usá-lo, você deve carregá-lo diretamente do Winshfhc.dll pelo ordinal 101.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (versão 5,1 ou posterior)</dt> </dl> |



 

 




