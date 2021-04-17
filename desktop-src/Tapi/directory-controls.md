---
description: O diagrama a seguir ilustra os principais objetos envolvidos nos controles de diretório de reunião TAPI 3. As interfaces mostradas são vinculadas às páginas de referência relevantes.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Controles de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789872"
---
# <a name="directory-controls"></a>Controles de diretório

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O diagrama a seguir ilustra os principais objetos envolvidos nos controles de diretório de reunião TAPI 3. As interfaces mostradas são vinculadas às páginas de referência relevantes.

![interfaces e objetos de controle do diretório de reunião](images/renddir.png)

A interface de controle de diretório principal é [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), que deve ser criada chamando **CoCreateInstance**. O objeto de reunião expõe métodos para obter listas de diretórios disponíveis e criar novos diretórios ou objetos de diretório.

Um diretório reside em um servidor e é uma lista de objetos de diretório, juntamente com informações descritivas. Os métodos associados ao [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) podem obter informações associadas ao diretório como um todo, como se ele é um diretório ILS.

Um objeto de diretório pode representar uma conferência ou um usuário. A interface [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) fornece métodos que podem recuperar ou modificar informações genéricas para um objeto de diretório, como o endereço de discagem.

As informações de conferência e de usuário, como a URL de uma conferência ou o telefone IP primário de um usuário, são manipuladas por métodos fornecidos nas interfaces [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) e [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .

 

 



