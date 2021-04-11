---
description: Defina para aplicativos recursos bem conhecidos usando a função AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes de SID de recurso (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172317"
---
# <a name="capability-sid-constants"></a>Constantes de SID de recurso

As constantes de SID de funcionalidade definem os recursos bem conhecidos do para aplicativos usando a função [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**recurso de segurança de \_ \_ cliente de Internet \_**
</dt> <dd> <dl> <dt>

(0x00000001l)
</dt> <dt>



Uma conta tem acesso à Internet de um computador cliente.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**funcionalidade de segurança \_ \_ servidor de cliente de Internet \_ \_**
</dt> <dd> <dl> <dt>

(0x00000002L)
</dt> <dt>



Uma conta tem acesso à Internet a partir dos computadores cliente e servidor.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_ \_ \_ servidor cliente de rede \_ privada \_ do recurso de segurança**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Uma conta tem acesso à Internet de uma rede privada.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_biblioteca de \_ imagens de recursos de segurança \_**
</dt> <dd> <dl> <dt>

(0x00000004L)
</dt> <dt>



Uma conta tem acesso à biblioteca de imagens.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_biblioteca de \_ vídeos de recursos de segurança \_**
</dt> <dd> <dl> <dt>

(0x00000005L)
</dt> <dt>



Uma conta tem acesso à biblioteca de vídeos.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_biblioteca de \_ música do recurso de segurança \_**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Uma conta tem acesso à biblioteca de músicas.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**\_biblioteca de \_ documentos de recursos de segurança \_**
</dt> <dd> <dl> <dt>

(0x00000007L)
</dt> <dt>



Uma conta tem acesso à biblioteca de documentação.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_ \_ autenticação corporativa do recurso de segurança \_**
</dt> <dd> <dl> <dt>

(0x00000008L)
</dt> <dt>



Uma conta tem acesso às credenciais padrão do Windows.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**recursos de segurança \_ \_ compartilhados \_ certificados de usuário \_**
</dt> <dd> <dl> <dt>

(0x00000009L)
</dt> <dt>



Uma conta tem acesso aos certificados de usuário compartilhados.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ armazenamento removível do recurso de segurança \_**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Uma conta tem acesso ao armazenamento removível.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Ao construir um SID de recurso, você precisa incluir a autoridade do pacote, a \_ \_ autoridade do pacote do aplicativo de segurança \_ {0,0,0,0,0,15} , na chamada para a função [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) . Além disso, você precisa da contagem base RID e RID para os recursos internos, o \_ \_ RID base de recurso de segurança \_ (0x00000003L) e a \_ contagem de RID de recurso interno de segurança \_ \_ \_ (2L).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

