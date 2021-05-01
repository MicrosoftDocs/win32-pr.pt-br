---
title: Inicialização Medida
description: Inicialização Medida
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314337"
---
# <a name="measured-boot"></a>Inicialização Medida

## <a name="platforms"></a>Plataformas

 **Clientes** -Windows 8  
**Servidores** -Windows Server 2012  



## <a name="description"></a>Descrição

Como o software antimalware (AM) se tornou melhor e melhor na detecção de malware de tempo de execução, os invasores também estão se tornando melhores na criação de rootkits que podem se esconder da detecção. Detectar malwares que iniciam no início do ciclo de inicialização é um desafio que a maioria dos fornecedores nos atendem de maneira programada. Normalmente, eles criam hackers do sistema que não têm suporte no sistema operacional do host e podem realmente resultar na colocação do computador em um estado instável. Até este ponto, o Windows não forneceu uma boa maneira para que eu detecte e resolva essas ameaças de inicialização antecipada. O Windows 8 apresenta um novo recurso chamado inicialização medida, que mede cada componente, do firmware até os drivers de inicialização, armazena essas medidas no Trusted Platform Module (TPM) no computador e disponibiliza um log que pode ser testado remotamente para verificar o estado de inicialização do cliente.

## <a name="manifestation"></a>Manifestação

O recurso de inicialização medido fornece software com um log confiável (resistente à falsificação e violação) de todos os componentes de inicialização que começaram antes do software. O software AM pode usar o log para determinar se os componentes que foram executados antes de serem confiáveis ou se estão infectados com malware. O software AM no computador local pode enviar o log para um servidor remoto para avaliação. O servidor remoto pode iniciar ações de correção interagindo com software no cliente ou por meio de mecanismos fora de banda, conforme apropriado.

## <a name="mitigation"></a>Atenuação

Em cenários empresariais, o administrador do sistema tem o controle de como as informações de inicialização são usadas. Em cenários de usuário final, por exemplo, o banco online, o consumidor deve optar por usar a inicialização medida para o serviço específico.

## <a name="solution"></a>Solução

Um white paper está sendo preparado para detalhar as APIs e as chamadas de função que devem ser feitas para vários cenários de inicialização medidos.

 

 




