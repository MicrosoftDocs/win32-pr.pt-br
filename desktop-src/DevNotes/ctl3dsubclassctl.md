---
description: Subclasses de um controle individual, a menos que o controle seja exibido em uma caixa de diálogo.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Função Ctl3dSubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749510"
---
# <a name="ctl3dsubclassctl-function"></a>Função Ctl3dSubclassCtl

Subclasses de um controle individual, a menos que o controle seja exibido em uma caixa de diálogo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela de controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se o controle tiver uma subclasse com êxito; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ctl3dUnsubclassCtl**](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
