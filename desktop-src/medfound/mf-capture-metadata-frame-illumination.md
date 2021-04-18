---
description: Um valor que indica se um quadro foi capturado usando a iluminação de infravermelho ativo (IR).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Atributo MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763929"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>\_Atributo de \_ iluminação de quadro de metadados de captura MF \_ \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Um valor que indica se um quadro foi capturado usando a iluminação de infravermelho ativo (IR).

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Esse atributo é um bitmask. É um valor de 64 bits para compatibilidade com versões anteriores.

A iluminação ativa é quando um dispositivo tem um emissor de luz próximo à câmera IR emitindo um feixe de luz para iluminar a cena, normalmente emitindo luz de IR para que não incomodar os olhos humanos. Defina valor como (valor & 0x1)! = 0 se o quadro foi capturado quando a iluminação ativa estava ativada e definida (valor & 0x1) = = 0 se a iluminação ativa estava desligada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                      |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




