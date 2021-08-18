---
description: As informações do usuário são um buffer que pode ser transmitido de uma extremidade de uma conexão para outra. Essas informações são específicas para o padrão ISDN Q.931. Consulte a documentação dos provedores de serviços sobre o significado e o uso desses dados.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Informações do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203b0b466d1b0b3f9da93cfefc5da737865da3cf5d40921dae6c969bfc9b9752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975286"
---
# <a name="user-user-information"></a>Informações do usuário

As informações do usuário são um buffer que pode ser transmitido de uma extremidade de uma conexão para outra. Essas informações são específicas para o padrão ISDN Q.931. Consulte a documentação do provedor de serviços sobre o significado e o uso desses dados.

Nem todos os provedores de serviços suportam o uso dessas informações.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** e **dwCallDataOffset** membros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

**TAPI 3.x: **[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), chamado com o membro **\_ USERUSERINFO CIB** de [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
