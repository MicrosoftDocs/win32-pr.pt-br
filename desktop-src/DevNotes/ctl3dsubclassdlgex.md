---
description: Subclasses de todos os controles em uma caixa de diálogo e na própria janela de diálogo.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Função Ctl3dSubclassDlgEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: aeacdf75e20e2d3521405c20b52d29a466c5fe9a063d70e5acb3c0597934ab9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162127"
---
# <a name="ctl3dsubclassdlgex-function"></a>Função Ctl3dSubclassDlgEx

Subclasses de todos os controles em uma caixa de diálogo e na própria janela de diálogo.

## <a name="syntax"></a>Sintaxe


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndDlg* 
</dt> <dd>

Um alça para a janela da caixa de diálogo.

</dd> <dt>

*grbit* 
</dt> <dd>

Os tipos de controle a serem subclasses. Esse valor pode ser qualquer um dos seguintes.



| Valor                                                                                                                                                                                                                                     | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D \_ BOTÕES**</dt> <dt>0x0001</dt> </dl>                 | Botões de subclasse.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D \_ LISTBOXES**</dt> <dt>0x0002</dt> </dl>           | Caixas de listagem de subclasse.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D \_ EDITS**</dt> <dt>0x0004</dt> </dl>                       | Controles de edição de subclasse.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D \_ ComBOS**</dt> <dt>0x0008</dt> </dl>                    | Caixas de combinação de subclasse.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D \_ STATICTEXTS**</dt> <dt>0x0010</dt> </dl>     | Controles de texto estático de subclasse.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D \_ STATICFRAMES**</dt> <dt>0x0020</dt> </dl>  | Quadros estáticos de subclasse.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D \_ TODOS**</dt> <dt>os 0xffff</dt> </dl>                             | Subclasse todos os controles.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt> </dl> | Não faça a subclasse da janela da caixa de diálogo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a função for bem-sucedida; caso contrário, retornará **FALSE.**

## <a name="remarks"></a>Comentários

Essa função é especialmente útil em aplicativos baseados em C++.

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
