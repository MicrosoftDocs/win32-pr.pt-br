---
description: Subclasses de um controle individual, a menos que o controle apareça em uma caixa de diálogo.
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
ms.openlocfilehash: f1d25bdc189ad80f1976ee76cc7f9909d099f34c8a88b83771ebf3f297c78934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654476"
---
# <a name="ctl3dsubclassctl-function"></a>Função Ctl3dSubclassCtl

Subclasses de um controle individual, a menos que o controle apareça em uma caixa de diálogo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Um alça para a janela de controle.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o controle for subclasse com êxito; caso contrário, retornará **FALSE.**

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Ctl3dUnsubclassCtl**](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
