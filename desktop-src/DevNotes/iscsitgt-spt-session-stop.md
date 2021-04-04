---
description: Usado com o IOCTL \_ da \_ miniporta SCSI do IOCTL e o \_ código de controle do 0x101 (CTLCODE ISCSITGT \_ SPT \_ Session \_ end) para interromper uma sessão.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Estrutura de ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103837716"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>\_Estrutura de \_ interrupção de sessão ISCSITGT SPT \_

\[A estrutura a seguir está disponível para uso no Windows Server 2012 R2. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Usado com o IOCTL da [**\_ \_ miniporta SCSI**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) do IOCTL e o \_ código de controle do 0x101 (CTLCODE ISCSITGT \_ SPT \_ Session \_ end) para interromper uma sessão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a>Membros

<dl> <dt>

**Cabeçalho**
</dt> <dd>

Cabeçalho obrigatório.

</dd> <dt>

**ITNexusHandle**
</dt> <dd>

Um identificador opaco que representa uma sessão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/> |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                               |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Passagem de destino iSCSI](/powershell/module/iscsi)
</dt> <dt>

[**\_controle de e/s SRB \_**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
