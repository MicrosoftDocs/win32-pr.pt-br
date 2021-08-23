---
description: A finalidade de uma DLL DOES é fornecer procedimentos personalizáveis de autenticação e identificação do usuário. O PADRÃO DEIS faz isso delegar o monitoramento de eventos SAS para o Winlogon, que recebe e processa ASS (sequências de atenção segura) CTL+ALT+DEL.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dad8917a24100fbf5c6c36eab3bbfc5b67baf62b378f9207626378fe864b672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623136"
---
# <a name="gina"></a>Gina

O [*ÂMBITO*](/windows/desktop/SecGloss/g-gly) opera no [*contexto*](/windows/desktop/SecGloss/c-gly) do processo [*winlogon*](/windows/desktop/SecGloss/w-gly) e, como tal, a DLL DOLP é carregada muito no início do processo de inicialização. A DLL DOEI deve seguir as regras para que a integridade do sistema seja mantida, especialmente em relação à interação com o usuário.

> [!Note]  
> As DLLs DE VALOR são ignoradas no Windows Vista.

 

O uso mais comum do SEMPRE é se comunicar com um dispositivo externo, como um leitor de cartão [*inteligente.*](/windows/desktop/SecGloss/r-gly) É essencial definir o parâmetro start para o driver de dispositivo para o sistema (Winnt.h: SERVICE SYSTEM START) para garantir que o driver seja carregado no momento em que oLP for \_ \_ invocado.

A finalidade de uma DLL DOES é fornecer procedimentos personalizáveis de autenticação e identificação do usuário. O PADRÃO DEIS faz isso delegar o monitoramento de eventos SAS para o Winlogon, que recebe e processa ASS [*(sequências*](/windows/desktop/SecGloss/s-gly) de atenção segura) CTL+ALT+DEL. Um CUSTOM é responsável por configurar a si mesmo para receber eventos SAS (diferente do evento padrão CTRL+ALT+DEL SAS) e notificar o Winlogon quando ocorrerem eventos SAS. O Winlogon avaliará seu estado para determinar o que é necessário para processar a SAS do DYNAMIC personalizada. Esse processamento geralmente inclui chamadas para as funções de processamento de SAS do SEMPRE.

Para obter informações sobre funções específicas de exportação [DELP,](authentication-functions.md)consulte Funções de exportação DE EXPORT. Para obter informações sobre como usar estruturas DEIS para passar informações, consulte [Estruturas DEIS.](authentication-structures.md)



| Tópico                                                                             | Descrição                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Carregando e executando uma DLL DE LTD](loading-and-running-a-gina-dll.md)<br/>   | Qual valor de chave do Registro deve ser alterado para carregar e executar uma DLL CUSTOM CUSTOM.<br/> |
| [Como criar e testar uma DLL DE LTD](building-and-testing-a-gina-dll.md)<br/> | Como testar uma DLL DE LTD.<br/>                                              |



 

 

