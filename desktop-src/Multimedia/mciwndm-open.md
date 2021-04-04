---
title: Mensagem de MCIWNDM_OPEN (VFW. h)
description: A mensagem de abertura do MCIWNDM \_ abre um dispositivo MCI e o associa a uma janela MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- Multimídia do Windows de mensagem MCIWNDM_OPEN
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085441"
---
# <a name="mciwndm_open-message"></a>MCIWNDM \_ Abrir mensagem

A mensagem de **\_ abertura do MCIWNDM** abre um dispositivo MCI e o associa a uma janela MCIWnd. Para dispositivos MCI que usam arquivos de dados, essa macro também pode abrir um arquivo de dados especificado, nomear um novo arquivo a ser criado ou exibir uma caixa de diálogo para permitir que o usuário selecione um arquivo a ser aberto. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Sinalizadores associados ao dispositivo ou ao arquivo a ser aberto. O \_ novo sinalizador MCIWNDOPENF especifica que um novo arquivo deve ser criado com o nome especificado em **szFile**.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo identificando o nome do nome do dispositivo ou do MCI a ser aberto. Especifique 1 para esse parâmetro para exibir a caixa de diálogo abrir.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





