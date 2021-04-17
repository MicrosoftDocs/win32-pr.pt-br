---
description: Os provedores gerenciam volumes em execução e criam cópias de sombra deles sob demanda.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb336dbb51fcbd715ea236ecdc0c62d81daf29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811384"
---
# <a name="providers"></a>Provedores

Os [*provedores*](vssgloss-p.md) gerenciam volumes em execução e criam cópias de sombra deles sob demanda.

Em resposta a uma solicitação de um solicitante, um provedor gera eventos COM para sinalizar aplicativos de uma cópia de sombra em vigor e, em seguida, cria e mantém essa cópia até que ela não seja mais necessária.

Enquanto uma cópia de sombra está em existência, o provedor cria um ambiente onde há efetivamente duas cópias independentes de qualquer volume que tenha sido copiado por sombra: um disco em execução que está sendo usado e atualizado normalmente, a outra cópia que é fixa e estável para backup.

Embora um provedor padrão seja fornecido como parte do Windows, outros fornecedores são livres para fornecer suas próprias implementações otimizadas para suas próprias ofertas de hardware e software de armazenamento.

Do ponto de vista de um desenvolvedor de aplicativos de usuário final ou backup/restauração, todos os provedores terão a mesma interface (consulte [selecionando provedores](selecting-providers.md)).

Todos os provedores devem ser capazes de fazer o seguinte:

-   Interceptar solicitações de e/s entre o sistema de arquivos e o sistema de armazenamento em massa subjacente.
-   Capture e recupere o status de um volume no momento da cópia de sombra, mantendo uma exibição "pontual" dos arquivos no disco sem operações parciais de e/s refletidas em seu estado.
-   Use essa exibição "pontual" para expor (minimamente para aplicativos habilitados para VSS) um volume virtual que contém os dados copiados de sombra.

Dependendo de como isso é feito, um provedor pode ser de um dos três tipos:

-   [Provedor do sistema](#system-provider)
-   [Provedores de software](#software-providers)
-   [Provedores de hardware](#hardware-providers)

## <a name="system-provider"></a>Provedor do sistema

Um provedor de cópia de sombra, o [*provedor do sistema*](vssgloss-s.md), é fornecido como parte padrão de uma instalação do sistema operacional Windows. Atualmente, o provedor do sistema é uma instância específica de um provedor de software. No entanto, isso pode ser alterado no futuro.

Para manter uma exibição "pontual" de um volume contido na cópia de sombra, o provedor do sistema usa uma técnica de copiar na gravação. Cópias dos setores em disco que foram modificados (chamadas de "diffs") desde o início da criação da cópia de sombra são armazenadas em uma área de armazenamento de cópia de sombra.

Portanto, o provedor do sistema pode expor o volume ativo, que pode ser gravado e lido normalmente, e aplicar as "diferenças" aos dados do volume ativo para expor efetivamente os dados congelados da cópia de sombra.

Para o provedor do sistema, a área de armazenamento de cópia de sombra deve estar em um volume NTFS. O volume a ser copiado em sombra não precisa ser um volume NTFS, mas pelo menos um volume montado no sistema deve ser um volume NTFS.

## <a name="software-providers"></a>Provedores de software

Os provedores de cópia de sombra de software interceptam e processam solicitações de e/s em uma camada de software entre o sistema de arquivos e o software do Gerenciador de volumes. Esses provedores são implementados como um componente DLL do modo de usuário e pelo menos um driver de dispositivo em modo kernel, normalmente (mas não necessariamente) um driver de filtro de armazenamento. O trabalho de criar essas cópias de sombra é feito no software.

Um provedor de cópia de sombra de software deve manter uma exibição "pontual" de um volume, tendo acesso a um conjunto de arquivos que podem ser usados para recriar com precisão o status do volume antes da cópia de sombra. Um exemplo disso é a técnica de copiar em gravação do provedor do sistema.

No entanto, o VSS não faz nenhuma restrição sobre a técnica que os provedores de software usam para criar e manter cópias de sombra, e fornecedores de terceiros são livres para implementar seus provedores de software como eles veem.

Além disso, o VSS oferece suporte para grande parte da funcionalidade dos provedores de cópia de sombra de software, como a definição do ponto no tempo, a sincronização de dados e a liberação, fornecendo uma interface comum para aplicativos de backup e o gerenciamento da cópia de sombra.

Um provedor de software, por definição, será aplicável a uma variedade maior de plataformas de armazenamento que um provedor de hardware, e deve ser capaz de trabalhar com discos básicos ou volumes lógicos igualmente bem. Essa generalidade sacrifica o desempenho que pode estar disponível implementando cópias de sombra em hardware e não usa nenhum recurso de captura de volume ou de espelhamento de arquivo específico do fornecedor.

## <a name="hardware-providers"></a>Provedores de hardware

Os provedores de cópia de sombra de hardware interceptam solicitações de e/s do sistema de arquivos no nível de hardware, trabalhando em conjunto com um adaptador ou controlador de armazenamento de hardware. O trabalho de criar a cópia de sombra é executado por um adaptador de host, dispositivo de armazenamento ou controlador RAID fora do sistema operacional.

Esses provedores são implementados como um componente DLL do modo de usuário que se comunica com o hardware que vai expor os dados de cópia de sombra: portanto, os provedores de cópia de sombra de hardware podem precisar chamar ou criar outros componentes do modo kernel.

Os provedores de hardware expõem para cópias de sombra do VSS de discos inteiros ou LUNs (unidades lógicas). Os solicitantes ainda lidam com cópias de sombra de volumes; todo o mapeamento de volume para disco é manipulado internamente pelo VSS. As cópias de sombra criadas por provedores de hardware de volumes que residem em discos dinâmicos têm um requisito específico: elas não podem ser importadas no mesmo sistema. Eles devem ser criados como transportáveis e importados em um segundo sistema.

Embora um provedor de cópia de sombra de hardware use a funcionalidade do VSS que define o ponto no tempo, permite a sincronização de dados, gerencia a cópia de sombra e fornece uma interface comum com aplicativos de backup, o VSS não especifica o mecanismo subjacente pelo qual o provedor de hardware produz e mantém cópias de sombra.

 

 



