---
description: A finalidade de uma DLL GINA é fornecer procedimentos de autenticação e identificação de usuário personalizáveis. A GINA padrão faz isso delegando o monitoramento de eventos SAS ao Winlogon, que recebe e processa as sequências de atenção seguro (SASs) de CTL + ALT + DEL.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662744"
---
# <a name="gina"></a>GINA

A [*Gina*](/windows/desktop/SecGloss/g-gly) opera no [*contexto*](/windows/desktop/SecGloss/c-gly) do processo do [*Winlogon*](/windows/desktop/SecGloss/w-gly) e, como tal, a dll Gina é carregada logo no início do processo de inicialização. A DLL GINA deve seguir as regras para que a integridade do sistema seja mantida, particularmente em relação à interação com o usuário.

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 

O uso mais comum da GINA é comunicar-se com um dispositivo externo, como um [*leitor*](/windows/desktop/SecGloss/r-gly)de cartão inteligente. É essencial definir o parâmetro Start para o driver de dispositivo como System (WinNT. h: início do \_ sistema de serviço \_ ) para garantir que o driver seja carregado até o momento em que a Gina é invocada.

A finalidade de uma DLL GINA é fornecer procedimentos de autenticação e identificação de usuário personalizáveis. A GINA padrão faz isso delegando o monitoramento de eventos SAS ao Winlogon, que recebe e processa as [*sequências de atenção seguro*](/windows/desktop/SecGloss/s-gly) (SASs) de CTL + ALT + del. Uma GINA personalizada é responsável por se configurar para receber eventos de SAS (além do evento de SAS CTRL + ALT + DEL) e notificar o Winlogon quando ocorrerem eventos de SAS. O Winlogon avaliará seu estado para determinar o que é necessário para processar a SAS da GINAção personalizada. Esse processamento geralmente inclui chamadas para as funções de processamento SAS da GINA.

Para obter informações sobre funções de exportação de GINA específicas, consulte [funções de exportação de Gina](authentication-functions.md). Para obter informações sobre como usar estruturas GINA para passar informações, consulte [estruturas Gina](authentication-structures.md).



| Tópico                                                                             | Descrição                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Carregando e executando uma DLL GINA](loading-and-running-a-gina-dll.md)<br/>   | Qual valor da chave do registro a ser alterado para carregar e executar uma DLL GINA personalizada.<br/> |
| [Criando e testando uma DLL GINA](building-and-testing-a-gina-dll.md)<br/> | Como testar uma DLL GINA.<br/>                                              |



 

 

