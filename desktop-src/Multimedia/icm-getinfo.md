---
title: ICM_GETINFO mensagem (Vfw.h)
description: A ICM GETINFO consulta um driver de compactação de vídeo para retornar uma \_ descrição de si mesmo em uma estrutura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO mensagem Windows Multimídia
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
ms.openlocfilehash: 173f510642b807a0e4c4a8c5c84d6d4de2aa7ce55cc0707eccabf5421cf98a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690806"
---
# <a name="icm_getinfo-message"></a>\_ICM Mensagem GETINFO

A **ICM \_ GETINFO** consulta um driver de compactação de vídeo para retornar uma descrição de si mesmo em uma [**estrutura ICINFO.**](/windows/desktop/api/Vfw/ns-vfw-icinfo)


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Ponteiro para uma **estrutura ICINFO** para conter informações.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamanho, em bytes, de **ICINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o tamanho, em bytes, de [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ou zero se ocorrer um erro..

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos enviam essa mensagem para exibir uma lista dos nós instalados.

O driver deve preencher todos os membros da estrutura [**ICINFO,**](/windows/desktop/api/Vfw/ns-vfw-icinfo) exceto **szDriver**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Compactação de Vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





