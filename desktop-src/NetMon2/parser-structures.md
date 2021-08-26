---
description: Esta seção descreve estruturas que você pode usar para desenvolver analisadores. Essas estruturas são usadas por funções que você pode usar para desenvolver analisadores e funções que você pode usar para desenvolver analisadores ou especialistas.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Estruturas do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d54e02e26e9874f27f49312a84b4b643cc4b3bfdb0c6056f274e4febecf0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082526"
---
# <a name="parser-structures"></a>Estruturas do analisador

Esta seção descreve estruturas que você pode usar para desenvolver analisadores. Essas estruturas são usadas por funções que você pode usar para desenvolver analisadores e funções que você pode usar para desenvolver analisadores ou especialistas.



| Estrutura                                 | Descrição                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | Define os protocolos iniciais mais comumente usados.                                                                               |
| [ENTRYPOINTS](entrypoints.md)            | Especifica os ponteiros para os pontos de entrada para a DLL do analisador.                                                                      |
| [FOLLOWENTRY de PF \_](pf-followentry.md)     | Especifica o protocolo que segue o protocolo atual.                                                                       |
| [seguir do PF \_](pf-followset.md)         | Especifica o conjunto de protocolos que segue o protocolo atual.                                                               |
| [HANDOFFENTRY de PF \_](pf-handoffentry.md)   | Especifica o protocolo que passa para o protocolo atual ou o protocolo para o qual o protocolo atual é immãos.    |
| [teleentregador de PF \_](pf-handoffset.md)       | Especifica o conjunto de protocolos que são disponibilizados para o protocolo atual ou para o conjunto de protocolos que o protocolo atual transfere para o. |
| [PARSERDLLINFO de PF \_](pf-parserdllinfo.md) | Especifica o número de analisadores na DLL do analisador e informações sobre cada analisador.                                            |
| [PARSERINFO de PF \_](pf-parserinfo.md)       | Especifica informações sobre um analisador específico.                                                                                  |
| [BIT ROTULAdo \_](labeled-bit.md)           | Especifica identificadores, campos de bits ou sinalizadores.                                                                                        |
| [BYTE ROTULAdo \_](labeled-byte.md)         | Especifica um par de rótulos de **byte** .                                                                                                |
| [RÓTULO \_ DWORD](labeled-dword.md)       | Especifica um par de rótulos **DWORD** .                                                                                               |
| [palavra ROTULAda \_](labeled-word.md)         | Especifica um par de rótulos de **palavras** .                                                                                                |
| [PROPERTYINFO](propertyinfo.md)          | Especifica as propriedades que o analisador de protocolo requer para descrever os quadros.                                                  |
| [PROPERTYINST](propertyinst.md)          | Especifica uma instância de uma propriedade em um quadro.                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | Especifica uma instância de propriedade de forma livre e estendida.                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | Especifica um protocolo.                                                                                                           |
| [AMPLITUDE](range.md)                        | Especifica um intervalo para um número.                                                                                                 |
| [SET](set.md)                            | Especifica uma tabela de valores para uma propriedade.                                                                                     |



 

Para obter informações sobre as funções usadas para desenvolver DLLs do analisador, consulte os tópicos a seguir.



| Para obter informações sobre                                         | Consulte                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Funções que as DLLs do analisador exportam.                        | [Funções de exportação de DLL do analisador](parser-dll-export-functions.md)               |
| Funções que você pode usar para desenvolver DLLs do analisador.            | [Funções do analisador](parser-functions.md)                                     |
| Funções que você pode usar para desenvolver DLLs de analisador e especialistas. | [Funções comuns de expert e parser](expert-and-parser-common-functions.md) |



 

 

 



