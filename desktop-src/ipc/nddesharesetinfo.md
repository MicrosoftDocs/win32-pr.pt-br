---
description: Define informações de compartilhamento DDE. Isso geralmente é feito após a edição.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Função NDdeShareSetInfo (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761903"
---
# <a name="nddesharesetinfo-function"></a>Função NDdeShareSetInfo

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Define informações de compartilhamento DDE. Isso geralmente é feito após a edição.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor cujo DSDM deve ser modificado.

</dd> <dt>

*lpszShareName* \[ no\]
</dt> <dd>

O nome do nome do compartilhamento cujas informações serão modificadas. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*nLevel* \[ no\]
</dt> <dd>

O nível de informações. Esse parâmetro deve ser 2.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Um ponteiro para a estrutura [**NDDESHAREINFO**](nddeshareinfo-str.md) que especifica as informações de compartilhamento DDE a serem armazenadas no DSDM. Atualmente, as informações de compartilhamento DDE são modificadas como um todo, ou seja, nenhuma edição parcial é feita. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*cBufSize* \[ no\]
</dt> <dd>

O tamanho do buffer *lpBuffer* , em bytes.

</dd> <dt>

*sParmNum* \[ no\]
</dt> <dd>

O índice de parâmetro a ser modificado. A implementação atual não dá suporte à modificação parcial; Portanto, esse parâmetro deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeShareSetInfoW** (Unicode) e **NDdeShareSetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




