---
description: A \_ estrutura de solicitação de e/s scartar \_ inicia uma estrutura de informações de controle de protocolo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: Estrutura de SCARD_IO_REQUEST (Winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: 9a377643e794b679be593bb99b8750698c92dd3aa8abacd79bfdb1c478c9c7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918882"
---
# <a name="scard_io_request-structure"></a>\_Estrutura de solicitação de e/s scartar \_

A estrutura de **\_ \_ solicitação de e/s scartar** inicia uma estrutura de informações de controle de protocolo. Qualquer informação específica do protocolo segue imediatamente essa estrutura. O comprimento total da estrutura deve estar alinhado com o tamanho da palavra da arquitetura de hardware subjacente. Por exemplo, no Win32, o comprimento de qualquer informação de PCI deve ser um múltiplo de quatro bytes para que ele se alinhe em um limite de 32 bits.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwProtocol**
</dt> <dd>

Protocolo em uso.

</dd> <dt>

**cbPciLength**
</dt> <dd>

Comprimento, em bytes, da estrutura **de \_ \_ solicitação de e/s scartar** , além das informações específicas de PCI a seguir.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Winsmcrd. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




