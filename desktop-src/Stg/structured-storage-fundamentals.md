---
title: Conceitos básicos de armazenamento estruturado
description: O armazenamento estruturado fornece o equivalente a um sistema de arquivos completo para armazenar objetos.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Strctd de armazenamento estruturado STG, conceitos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823829"
---
# <a name="structured-storage-fundamentals"></a>Conceitos básicos de armazenamento estruturado

O armazenamento estruturado fornece o equivalente a um sistema de arquivos completo para armazenar objetos por meio dos elementos listados na tabela a seguir.



| Elemento                                                                  | Descrição                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaces de armazenamento estruturado](structured-storage-interfaces.md)       | As interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)e [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) , juntamente com um conjunto de interfaces relacionadas —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)e [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). |
| [Funções de API de armazenamento estruturado](structured-storage-api-functions.md) | APIs auxiliares que facilitam uma implementação de armazenamento estruturado, bem como um segundo conjunto de APIs para arquivos compostos; Essa é a implementação COM das interfaces de armazenamento estruturado. COM também fornece um conjunto de estruturas de suporte e valores de enumeração usados para organizar parâmetros para métodos de interface e APIs.                              |
| [Modos de acesso de armazenamento estruturado](structured-storage-access-modes.md)   | Um conjunto de modos de acesso para controlar o acesso a arquivos compostos.                                                                                                                                                                                                                                                                                                 |



 

 

 