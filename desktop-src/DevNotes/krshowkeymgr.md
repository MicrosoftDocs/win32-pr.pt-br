---
description: Abre a caixa de diálogo do Gerenciador de chaves na interface do usuário.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: Função KRShowKeyMgr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748355"
---
# <a name="krshowkeymgr-function"></a>Função KRShowKeyMgr

\[Essa função está incluída apenas no Windows XP. No momento, ele não está incluído em nenhuma outra versão do Windows, nem é esperado que ele seja incluído em versões futuras do Windows.\]

Abre a caixa de diálogo do Gerenciador de chaves na interface do usuário.

## <a name="syntax"></a>Sintaxe


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwParent* 
</dt> <dd>

Um identificador para a janela pai da caixa de diálogo. Este parâmetro pode ser **NULL**.

</dd> <dt>

*hInstance* 
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como **nulo**.

</dd> <dt>

*pszCmdLine* 
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como **nulo**.

</dd> <dt>

*CmdShow* 
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
