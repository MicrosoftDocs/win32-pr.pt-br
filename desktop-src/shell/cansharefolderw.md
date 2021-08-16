---
description: Usado para determinar se a opção compartilhar esta pasta deve ser mostrada na exibição da Web.
title: Função CanShareFolderW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 7013c6ae825c34ae7d2dd7b9d507eac1e52c8d4e3a27182e5297e72ef13b4d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032864"
---
# <a name="cansharefolderw-function"></a>Função CanShareFolderW

\[essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

Usado para determinar se a opção **compartilhar esta pasta** deve ser mostrada na exibição da Web.

## <a name="syntax"></a>Sintaxe


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszPath* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres que especifica o caminho da pasta a ser testada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **STDAPI**

Os valores de retorno incluem o seguinte.



| Código/valor de retorno                                                                        | Descrição                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>     | O caminho apontado por *pszPath* especifica uma pasta que pode ser compartilhada.<br/>    |
| <dl> <dt>**\_falso**</dt> </dl>  | O caminho apontado por *pszPath* especifica uma pasta que não pode ser compartilhada.<br/> |
| <dl> <dt>Erro HRESULT</dt> </dl> | Ocorreu um erro.<br/>                                                     |



 

## <a name="remarks"></a>Comentários

Esta função não tem nenhum arquivo. lib associado. Você deve usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usá-lo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CanShareFolderW** (Unicode)<br/>                                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
