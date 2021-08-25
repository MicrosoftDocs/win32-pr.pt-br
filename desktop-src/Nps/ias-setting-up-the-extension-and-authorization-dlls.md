---
title: Configurando as DLLs de extensão
description: Na inicialização, o NPS verifica o registro para obter uma lista de DLLs de terceiros a serem chamadas.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737d53bd25a28321c333e890a019af881ae54fa1c5ae92299b1776689f9abb74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962506"
---
# <a name="setting-up-the-extension-dlls"></a>Configurando as DLLs de extensão

> [!Note]  
> o IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

Na inicialização, o NPS verifica o registro para obter uma lista de DLLs de terceiros a serem chamadas.

Para configurar uma DLL de autenticação ou autorização em um servidor NPS, liste os caminhos para as DLLs em valores abaixo da seguinte chave do registro:

**HKLM \\ System \\ CurrentControlSet \\ Services \\ AuthSrv \\ Parameters\\**

Se as chaves **AuthSrv** e **Parameters** não existirem, crie-as.

O valor no qual listar as DLLs de extensão de autenticação é:

**ExtensionDLLs**

O valor no qual listar as DLLs de extensão de autorização é:

**AuthorizationDLLs**

Os valores **ExtensionDLLs** e **AuthorizationDLLs** devem ser do tipo **reg \_ multi \_ sz**. Esse tipo permite listar várias DLLs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Invocando as DLLs de extensão](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Atributos de identificação de usuário](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 