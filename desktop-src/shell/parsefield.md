---
description: Lê uma linha de setup. inf e extrai o campo especificado da cadeia de caracteres.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Função parsefield (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 737602777e02e4cdf88d2e07e3037ae940d257036a03a415271e4a6e1291dc7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677924"
---
# <a name="parsefield-function"></a>Função parsefield

\[a função **parsefield** , no momento, deve estar disponível para uso na próxima versão do sistema operacional Microsoft Windows. Ele pode ser alterado ou indisponível nas versões subsequentes.\]

Lê uma linha de setup. inf e extrai o campo especificado da cadeia de caracteres.

## <a name="syntax"></a>Sintaxe


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szData* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR \***

Um ponteiro para a linha do setup. inf.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **int**

**Int** que indica qual campo deve ser extraído.

<dt>



  acima (0)


</dt> <dd>

Indica o campo antes de um sinal de igual (=).

</dd> <dt>



 (1)


</dt> <dd>

Indica o primeiro campo.

</dd> </dl> </dd> <dt>

*szBuf* \[ no\]
</dt> <dd>

Tipo: **LPTSTR \***

Um ponteiro para o buffer que recebe o campo extraído.

</dd> <dt>

*iBufLen* \[ no\]
</dt> <dd>

Tipo: **int**

**Int** que recebe o tamanho do buffer que recebe o campo extraído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **bool**

Retornará **true** se a função for bem-sucedida e **false** se falhar.

## <a name="remarks"></a>Comentários

Os campos na cadeia de caracteres devem ser separados por vírgulas.

Espaços à esquerda e à direita são removidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Util. h</dt> </dl>                             |
| Biblioteca<br/>                  | <dl> <dt>Shell32. lib</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 




