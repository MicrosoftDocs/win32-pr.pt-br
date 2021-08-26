---
title: Mensagem de ICM_GET (VFW. h)
description: o ICM \_ obter mensagem recupera um valor DWORD definido pelo aplicativo de um driver de compactação de vídeo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- mensagem de ICM_GET Windows multimídia
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8885faf7b0605378ace3004165004384a582c9d49a0a8ce047122c108b6cb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038726"
---
# <a name="icm_get-message"></a>ICM \_ OBTER mensagem

o **ICM \_ obter** mensagem recupera um valor **DWORD** definido pelo aplicativo de um driver de compactação de vídeo.


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Ponteiro para um bloco de memória a ser preenchido com o estado atual. Você também pode especificar **NULL** para determinar a quantidade de memória exigida pelas informações de estado.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Tamanho, em bytes, do bloco de memória.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna a quantidade de memória, em bytes, necessária para armazenar as informações de status.

## <a name="remarks"></a>Comentários

A estrutura usada para representar informações de estado é específica do driver e é definida pelo driver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





