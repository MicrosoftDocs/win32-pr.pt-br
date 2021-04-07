---
title: Mensagem de ICM_DECOMPRESSEX_QUERY (VFW. h)
description: A mensagem de consulta DECOMPRESSEX do ICM consulta \_ \_ um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode descompactar um formato de entrada específico para um formato de saída específico.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESSEX_QUERY
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824656"
---
# <a name="icm_decompressex_query-message"></a>\_Mensagem de \_ consulta ICM DECOMPRESSEX

A mensagem de **\_ \_ consulta DECOMPRESSEX do ICM** consulta um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode descompactar um formato de entrada específico para um formato de saída específico.


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Ponteiro para uma estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contém o formato de entrada.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se a descompactação especificada for suportada ou ICERR \_ BADFORMAT do contrário.

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

 

 





