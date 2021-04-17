---
description: Subclasses todos os controles em uma caixa de diálogo e na janela da caixa de diálogo.
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
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749530"
---
# <a name="ctl3dsubclassdlgex-function"></a>Função Ctl3dSubclassDlgEx

Subclasses todos os controles em uma caixa de diálogo e na janela da caixa de diálogo.

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

Um identificador para a janela da caixa de diálogo.

</dd> <dt>

*grbit* 
</dt> <dd>

Os tipos de controle a serem subclasses. Esse valor pode ser qualquer um dos seguintes.



| Valor                                                                                                                                                                                                                                     | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D \_**</dt> <dt>0X0001</dt> de botões </dl>                 | Botões de subclasse.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D \_**</dt> <dt>0X0002</dt> de caixas de listagem </dl>           | Caixas de listagem de subclasses.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D \_ EDITA**</dt> <dt>0x0004</dt> </dl>                       | Controles de edição de subclasse.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D \_**</dt> <dt>0X0008</dt> de combinação </dl>                    | Caixas de combinação de subclasse.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D \_ STATICTEXTS**</dt> <dt>0x0010</dt> </dl>     | Controles de texto estáticos de subclasse.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D \_ STATICFRAMES**</dt> <dt>0x0020</dt> </dl>  | Quadros estáticos de subclasse.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D \_ Todos os**</dt> <dt>0xFFFF</dt> </dl>                             | Subclasse todos os controles.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt> </dl> | Não faça a subclasse da janela de diálogo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Essa função é especialmente útil em aplicativos baseados em C++.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
