---
description: Usuário – as informações do usuário são um buffer que pode ser transmitido de uma extremidade de uma conexão para outra. Essas informações são específicas para o padrão ISDN Q. 931. Consulte a documentação dos provedores de serviços sobre o significado e o uso desses dados.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Usuário – informações do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506078"
---
# <a name="user-user-information"></a>Usuário – informações do usuário

Usuário – as informações do usuário são um buffer que pode ser transmitido de uma extremidade de uma conexão para outra. Essas informações são específicas para o padrão ISDN Q. 931. Consulte a documentação do provedor de serviços sobre o significado e o uso desses dados.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** e **dwCallDataOffset** membros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

* * TAPI 3. x: * *[**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), chamado com o **membro \_ UserUserInfo CIB** do [**\_ buffer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo:: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
