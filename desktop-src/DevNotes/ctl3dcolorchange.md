---
description: Manipula alterações de cores do sistema para aplicativos que usam CTL3D.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Função Ctl3dColorChange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: c9c3032bb7105a27b995c236e01ce5fc5c304de4108f6c996a5cbb5799be496d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654596"
---
# <a name="ctl3dcolorchange-function"></a>Função Ctl3dColorChange

Manipula alterações de cores do sistema para aplicativos que usam CTL3D.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Essa função deve ser chamada no procedimento da janela principal do aplicativo para a **mensagem \_ SYSCOLORCHANGE do WM** , como mostrado abaixo.

## <a name="examples"></a>Exemplos

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
