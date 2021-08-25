---
description: As funções a seguir são os pontos de entrada para DLLs especializadas e para chamadas do sistema operacional e Monitor de Rede.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funções de exportação de DLL especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327b36990ac377595b31b55ebc0ed57157fd8d411f690aff3378293f35e39e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911126"
---
# <a name="expert-dll-export-functions"></a>Funções de exportação de DLL especialista

As funções a seguir são os pontos de entrada para DLLs especializadas e para chamadas do sistema operacional e Monitor de Rede.



| Função                                   | Descrição                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Especialista em DllMain**](dllmain-expert.md)   | Indica que a DLL especializada foi carregada ou descarregada. Quando um processo carrega ou descarrega a DLL, o sistema operacional chama a [**função DllMain.**](/windows/desktop/Dlls/dllmain) |
| [**Registrar Especialista**](register-expert.md) | Determina informações básicas sobre o especialista na DLL. Monitor de Rede chama a **função Register.**                                                           |
| [**Configurar**](configure.md)             | Configura o especialista na DLL. Monitor de Rede chama a [**função Configurar.**](configure.md)                                                                 |
| [**Executar**](run.md)                         | Inicia o especialista dentro da DLL. Monitor de Rede chama a [**função**](run.md) Executar.                                                                                 |



 

Monitor de Rede também fornece estruturas, enumerações e funções auxiliares que o especialista pode chamar.



| Para obter informações sobre                                      | Consulte                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Funções auxiliares que podem ser chamadas por especialistas e analisadores | [Funções comuns de especialista e analisador](expert-and-parser-common-functions.md) |
| Funções auxiliares que são chamadas somente por especialistas           | [Funções de especialista](expert-functions.md)                                     |
| Estruturas que são usadas por funções especializadas               | [Estruturas de especialistas](expert-structures.md)                                   |
| Enumerações usadas por estruturas e funções especializadas       | [Enumerações de especialistas](expert-enumerations.md)                               |



 

 

 
