---
description: Defina para aplicativos recursos conhecidos usando a função AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes sid de funcionalidade (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37a06c0bd0115c4f7d05753825477b5de4948d1ddb9576aea46933a63cbf409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783210"
---
# <a name="capability-sid-constants"></a>Constantes sid de funcionalidade

As constantes de SID de funcionalidade definem para aplicativos recursos conhecidos usando a [**função AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**CLIENTE DE \_ INTERNET DE FUNCIONALIDADE DE \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x00000001L)
</dt> <dt>



Uma conta tem acesso à Internet de um computador cliente.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SERVIDOR \_ CLIENTE DA INTERNET DE FUNCIONALIDADE DE \_ \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x00000002L)
</dt> <dt>



Uma conta tem acesso à Internet dos computadores cliente e servidor.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SERVIDOR CLIENTE DE REDE PRIVADA DE FUNCIONALIDADE \_ \_ DE \_ \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Uma conta tem acesso à Internet de uma rede privada.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**BIBLIOTECA \_ DE IMAGENS DE FUNCIONALIDADE DE \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x00000004L)
</dt> <dt>



Uma conta tem acesso à biblioteca de imagens.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**BIBLIOTECA DE \_ VÍDEOS DE FUNCIONALIDADE DE \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x00000005L)
</dt> <dt>



Uma conta tem acesso à biblioteca de vídeos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**BIBLIOTECA \_ DE MÚSICA DE FUNCIONALIDADE DE \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Uma conta tem acesso à biblioteca de música.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**BIBLIOTECA \_ DE DOCUMENTOS DE FUNCIONALIDADE DE \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x00000007L)
</dt> <dt>



Uma conta tem acesso à biblioteca de documentação.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**FUNCIONALIDADE \_ DE SEGURANÇA \_ AUTENTICAÇÃO \_ CORPORATIVA**
</dt> <dd> <dl> <dt>

(0x00000008L)
</dt> <dt>



Uma conta tem acesso às credenciais Windows padrão.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**FUNCIONALIDADE \_ DE SEGURANÇA \_ \_ CERTIFICADOS DE USUÁRIO \_ COMPARTILHADOS**
</dt> <dd> <dl> <dt>

(0x00000009L)
</dt> <dt>



Uma conta tem acesso aos certificados de usuário compartilhados.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**ARMAZENAMENTO \_ REMOVÍVEL DE \_ FUNCIONALIDADE DE \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Uma conta tem acesso ao armazenamento removível.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Ao construir um SID de funcionalidade, você precisa incluir a autoridade de pacote, SECURITY APP PACKAGE AUTHORITY , na chamada para a função \_ \_ \_ {0,0,0,0,0,15} [**AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) Além disso, você precisa da contagem rid e RID base para as funcionalidades internas, SECURITY \_ CAPABILITY \_ BASE RID \_ (0x00000003L) e SECURITY \_ BUILTIN \_ CAPABILITY RID COUNT \_ \_ (2L).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



 

