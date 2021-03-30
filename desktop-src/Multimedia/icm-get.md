---
title: Mensagem de ICM_GET (VFW. h)
description: A mensagem de obtenção de ICM \_ recupera um valor DWORD definido pelo aplicativo de um driver de compactação de vídeo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- Multimídia do Windows de mensagem ICM_GET
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
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644398"
---
# <a name="icm_get-message"></a>\_Extrair mensagem do ICM

A mensagem de **\_ obtenção de ICM** recupera um valor **DWORD** definido pelo aplicativo de um driver de compactação de vídeo.


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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





