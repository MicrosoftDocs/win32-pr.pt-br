---
title: Estrutura de MCI_OVLY_WINDOW_PARMS (Mciapi. h)
description: A \_ estrutura de parâmetros da janela MCI OVLY \_ \_ contém informações de exibição de janela para o \_ comando de janela MCI para dispositivos de sobreposição de vídeo.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_WINDOW_PARMS
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917971"
---
# <a name="mci_ovly_window_parms-structure"></a>\_Estrutura de \_ parâmetros da janela OVLY MCI \_

A estrutura de **\_ parâmetros da \_ janela \_ MCI OVLY** contém informações de exibição de janela para o comando de [**\_ janela MCI**](mci-window.md) para dispositivos de sobreposição de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**hWnd**
</dt> <dd>

Identificador para exibir janela.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Janela-comando de exibição.

</dd> <dt>

**lpstrText**
</dt> <dd>

Legenda da janela.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**\_janela MCI**](mci-window.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

