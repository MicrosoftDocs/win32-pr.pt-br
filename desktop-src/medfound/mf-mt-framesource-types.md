---
description: Um valor que indica o tipo de sensor fornecido por uma fonte de quadro, como cor, infravermelho ou profundidade.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: Atributo MF_MT_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3cddc28db050ec3fdb55e47ca2ceb1bd24fb2813bdf90fce439843957a7ae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113766"
---
# <a name="mf_mt_framesource_types-attribute"></a>\_Atributo de \_ tipos de framery MF MT \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Um valor que indica o tipo de sensor fornecido por uma fonte de quadro, como cor, infravermelho ou profundidade.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse valor deve ser um membro da enumeração [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) . Para compatibilidade com versões anteriores, quando esse atributo não está definido em um tipo de mídia, supõe-se que **\_ MFFrameSourceTyes:: Color**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                      |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
