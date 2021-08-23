---
title: Provisionamento fino de unidades lógicas
description: Provisionamento fino de unidades lógicas
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- Lba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ed5385322601e633f79755fb192f1dce578f2bec0f944fa2f4f412c32d69a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935046"
---
# <a name="thin-provisioning-of-logical-units"></a>Provisionamento fino de unidades lógicas

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

Windows O Provisionamento Fino é uma interface para a solução de provisionamento de armazenamento de ponta a ponta. Para fornecer um serviço de provisionamento de armazenamento altamente disponível, escalonável e amigável, é necessário implementações robustas do host do servidor para o dispositivo de destino de armazenamento. O recurso de provisionamento fino do Windows fornece uma exibição síncrona dos dispositivos de armazenamento de provisionamento fino para o administrador do sistema, o gerenciador de IT e o administrador de armazenamento por meio da identificação de LUN (unidade lógica) provisionada de forma fina, notificação de limite, tratamento de esgotamento de recursos, recuperação de espaço e recuperação de estado de LBA (endereçamento de bloco lógico). O Windows de provisionamento fino apresenta um modelo de serviço de provisionamento de armazenamento robusto que pode ser aplicado a sistemas de armazenamento cliente-servidor, armazenamento de virtualização e serviços de armazenamento em nuvem. A Microsoft garantirá a alta qualidade do recurso de provisionamento fino impondo os requisitos Windows Kit de Certificação de Hardware de Provisionamento Fino para produtos de matriz de armazenamento.

A Windows de armazenamento de Provisionamento Fino:

-   Permite que os administradores de armazenamento criem um LUN maior com menos recursos de disco físico
-   Adiciona ou remove o recurso de disco físico sem interromper o serviço de provisionamento de armazenamento
-   Alerta os usuários sobre o uso do volume de armazenamento por meio da configuração de limite
-   Dá suporte ao provisionamento de armazenamento por meio da configuração do pool de armazenamento compartilhado
-   Aumenta ou diminui o tamanho do pool de armazenamento de acordo com a demanda e o uso do espaço de armazenamento

Resumo dos recursos Windows provisionamento fino:

-   Identificação de LUN de Provisionamento Fino
-   Lida com a notificação de limite, esgotamento de recursos temporários e esgotamento permanente de recursos
-   Armazenamento recuperação de espaço
-   Mapeando consultas de estado de blocos lógicos

## <a name="manifestation"></a>Manifestação

Sem a compreensão adequada dos identificado Windows para LUN de provisionamento dinâmico, o aplicativo pode falhar com um comportamento inesperado ou por uma causa desconhecida.

## <a name="using-thin-provisioning-luns"></a>Usando LUNs de provisionamento fino

Para usar LUNs provisionados de forma Windows 8 ou Windows Server 2012, os administradores de sistema e armazenamento devem estar cientes destes problemas:

-   Identificação de LUN de provisionamento fino; os administradores do sistema ou os usuários finais podem usar o Defrag e o utilitário Armazenamento Optimizer para identificar o tipo de mídia do dispositivo de armazenamento
-   Quando um evento de esgotamento de recursos permanente ou limite for atingido, Windows registrará um evento do sistema para alertar o administrador do sistema
-   Armazenamento recuperação de espaço pode ser executada manual ou automaticamente por notificação de exclusão de arquivo ou pelo agendador do otimizador de armazenamento
-   Armazenamento administrador deve implementar a notificação de limite para alertar o administrador do sistema ou o usuário final e evitar qualquer interrupção inesperada do serviço de armazenamento

## <a name="tests"></a>Testes

-   Armazenamento matriz deve receber um certificado Windows 8 provisionamento fino para dar suporte Windows recursos de Provisionamento Fino
-   Windows O Kit de Certificação de Hardware de Provisionamento Fino para a matriz de armazenamento será uma ferramenta de teste útil para verificar a capacidade da matriz de armazenamento para Windows suporte a recursos de Provisionamento Fino
-   Windows espera que o LUN de Provisionamento Fino e o LUN de Provisionamento Completo funcionem no mesmo sistema sem nenhum problema

## <a name="resources"></a>Recursos

-   [Especificação de comando do bloco T10 SCSI (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Serviços de Painel de Hardware](/windows-hardware/drivers/dashboard/)

 

 