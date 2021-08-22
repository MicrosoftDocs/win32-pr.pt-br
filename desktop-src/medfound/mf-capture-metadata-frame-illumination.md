---
description: Um valor que indica se um quadro foi capturado usando a iluminação de infravermelho ativo (IR).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Atributo MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23658f8f396a81180a074badc43e98d0f392fc355c1a81a4d1e731d132de12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973945"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>\_Atributo de \_ iluminação de quadro de metadados de captura MF \_ \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Um valor que indica se um quadro foi capturado usando a iluminação de infravermelho ativo (IR).

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Esse atributo é um bitmask. É um valor de 64 bits para compatibilidade com versões anteriores.

A iluminação ativa é quando um dispositivo tem um emissor de luz próximo à câmera IR emitindo um feixe de luz para iluminar a cena, normalmente emitindo luz de IR para que não incomodar os olhos humanos. Defina valor como (valor & 0x1)! = 0 se o quadro foi capturado quando a iluminação ativa estava ativada e definida (valor & 0x1) = = 0 se a iluminação ativa estava desligada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                      |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




