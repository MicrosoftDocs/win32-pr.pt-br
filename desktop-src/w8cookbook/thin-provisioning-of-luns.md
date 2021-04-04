---
title: Provisionamento dinâmico de unidades lógicas
description: Provisionamento dinâmico de unidades lógicas
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008503"
---
# <a name="thin-provisioning-of-logical-units"></a>Provisionamento dinâmico de unidades lógicas

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

O provisionamento dinâmico do Windows é uma interface para a solução de provisionamento de armazenamento de ponta a ponta. Para fornecer um serviço de provisionamento de armazenamento altamente disponível, escalonável e amigável requer implementações robustas do host do servidor para o dispositivo de destino de armazenamento. O recurso de provisionamento dinâmico do Windows fornece uma exibição síncrona dos dispositivos de armazenamento de provisionamento dinâmico para o administrador do sistema, o gerente de ti e o administrador de armazenamento por meio da identificação de LUN (unidade lógica), notificação de limite, tratamento de esgotamento de recursos e recuperação de estado LBA (Logical Block Addressing). O recurso de provisionamento dinâmico do Windows apresenta um modelo de serviço de provisionamento de armazenamento robusto que pode ser aplicado a sistemas de armazenamento de cliente-servidor, armazenamento de virtualização e serviços de armazenamento em nuvem. A Microsoft garantirá a alta qualidade do recurso de provisionamento dinâmico ao impor os requisitos do kit de certificação de hardware do provisionamento dinâmico do Windows para produtos de matriz de armazenamento.

A solução de armazenamento de provisionamento dinâmico do Windows:

-   Permite que os administradores de armazenamento criem um LUN maior com menos recursos de disco físico
-   Adiciona ou remove o recurso de disco físico sem interromper o serviço de provisionamento de armazenamento
-   Alerta os usuários sobre o uso do volume de armazenamento por meio da configuração de limite
-   Dá suporte ao provisionamento de armazenamento por meio da configuração do pool de armazenamento compartilhado
-   Aumenta ou diminui o tamanho do pool de armazenamento de acordo com a demanda e o uso do espaço de armazenamento

Resumo dos recursos de provisionamento fino do Windows:

-   Identificação de LUN de provisionamento dinâmico
-   Identificadores para notificação de limite, esgotamento de recursos temporários e esgotamento de recursos permanentes
-   Reclamação do espaço de armazenamento
-   Mapeamento de consultas de estado de blocos lógicos

## <a name="manifestation"></a>Manifestação

Sem a compreensão correta dos identificadores do Windows para o LUN de provisionamento dinâmico, o aplicativo pode falhar com comportamento inesperado ou devido a uma causa desconhecida.

## <a name="using-thin-provisioning-luns"></a>Usando LUNs de provisionamento dinâmico

Para usar LUNs com provisionamento dinâmico no Windows 8 ou no Windows Server 2012, os administradores de sistema e armazenamento devem estar cientes dessas questões:

-   Identificação de LUN de provisionamento dinâmico; os administradores do sistema ou os usuários finais podem usar a desfragmentação e o utilitário de otimização de armazenamento para identificar o tipo de mídia do dispositivo de armazenamento
-   Quando um evento de esgotamento de recursos permanente ou limite for atingido, o Windows registrará um evento do sistema para alertar o administrador do sistema
-   A reclamação do espaço de armazenamento pode ser realizada manual ou automaticamente pela notificação de exclusão de arquivo ou pelo Agendador do otimizador de armazenamento
-   O administrador de armazenamento deve implementar a notificação de limite para alertar o administrador do sistema ou o usuário final e evitar qualquer interrupção inesperada do serviço de armazenamento

## <a name="tests"></a>Testes

-   A matriz de armazenamento deve receber o certificado de provisionamento dinâmico do Windows 8 para dar suporte aos recursos de provisionamento fino do Windows
-   O kit de certificação de hardware de provisionamento dinâmico do Windows para matriz de armazenamento será uma ferramenta de teste útil para verificar a capacidade da matriz de armazenamento para o suporte ao recurso de provisionamento thin do Windows
-   O Windows espera que o LUN de provisionamento thin e o LUN de provisionamento completo funcionem no mesmo sistema sem qualquer problema

## <a name="resources"></a>Recursos

-   [Especificação de comando de bloco T10 SCSI (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Serviços de painel de hardware](/windows-hardware/drivers/dashboard/)

 

 