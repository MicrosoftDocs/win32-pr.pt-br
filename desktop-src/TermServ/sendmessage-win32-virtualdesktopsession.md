---
title: Método SendMessage da classe Win32_VirtualDesktopSession
description: Envie uma mensagem para o usuário por meio da sessão de área de trabalho virtual.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Método SendMessage Serviços de Área de Trabalho Remota
- Método SendMessage Serviços de Área de Trabalho Remota, classe Win32_VirtualDesktopSession
- Classe Win32_VirtualDesktopSession Serviços de Área de Trabalho Remota, método SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159d9c8b4e8c4b5086fff9c4fc6c67c0a6e33464eeefee77d15a620b157bd55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988146"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>Método SendMessage da classe Win32 \_ VirtualDesktopSession

Envie uma mensagem para o usuário por meio da sessão de área de trabalho virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Título* \[ do no\]
</dt> <dd>

O título do mensagens das.

</dd> <dt>

*Mensagem* \[ de no\]
</dt> <dd>

O conteúdo da mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_VirtualDesktopSession Win32**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





