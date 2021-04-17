---
title: Mensagem de ICM_GETINFO (VFW. h)
description: A \_ mensagem ICM GetInfo consulta um driver de compactação de vídeo para retornar uma descrição de si mesmo em uma estrutura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- Multimídia do Windows de mensagem ICM_GETINFO
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759628"
---
# <a name="icm_getinfo-message"></a>\_Mensagem ICM GETinfo

A mensagem **ICM \_ GetInfo** consulta um driver de compactação de vídeo para retornar uma descrição de si mesmo em uma estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Ponteiro para uma estrutura **ICINFO** para conter informações.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de **ICINFO**.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o tamanho, em bytes, de [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ou zero se ocorrer um erro.

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos enviam essa mensagem para exibir uma lista dos compactadores instalados.

O driver deve preencher todos os membros da estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) , exceto **szDriver**.

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

 

 





