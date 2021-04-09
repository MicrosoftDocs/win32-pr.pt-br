---
description: As funções a seguir são os pontos de entrada para DLLs de especialistas e chamadas do sistema operacional e Monitor de Rede.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funções de exportação de DLL de especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920711"
---
# <a name="expert-dll-export-functions"></a>Funções de exportação de DLL de especialista

As funções a seguir são os pontos de entrada para DLLs de especialistas e chamadas do sistema operacional e Monitor de Rede.



| Função                                   | Descrição                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Especialista em DllMain**](dllmain-expert.md)   | Indica que a DLL de especialista foi carregada ou descarregada. Quando um processo carrega ou descarrega a DLL, o sistema operacional chama a função [**DllMain**](/windows/desktop/Dlls/dllmain) . |
| [**Registrar especialista**](register-expert.md) | Determina as informações básicas sobre o especialista dentro da DLL. Monitor de Rede chama a função de **registro** .                                                           |
| [**Configurar**](configure.md)             | Configura o especialista dentro da DLL. Monitor de Rede chama a função [**Configurar**](configure.md) .                                                                 |
| [**Executar**](run.md)                         | Inicia o especialista na DLL. Monitor de Rede chama a função [**Run**](run.md) .                                                                                 |



 

O Monitor de Rede também fornece estruturas, enumerações e funções auxiliares que o especialista pode chamar.



| Para obter informações sobre                                      | Consulte                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Funções auxiliares que podem ser chamadas por especialistas e analisadores | [Funções comuns de expert e parser](expert-and-parser-common-functions.md) |
| Funções auxiliares que são chamadas apenas por especialistas           | [Funções de especialista](expert-functions.md)                                     |
| Estruturas que são usadas por funções de especialista               | [Estruturas de especialistas](expert-structures.md)                                   |
| Enumerações usadas por estruturas e funções de especialistas       | [Enumerações de especialistas](expert-enumerations.md)                               |



 

 

 
