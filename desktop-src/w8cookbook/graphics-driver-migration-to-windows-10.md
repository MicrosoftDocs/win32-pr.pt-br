---
title: Migração de driver gráfico para Windows 10
description: Windows 10 A mídia Windows 10, como seu antecessor, Windows 8.1, não tem drivers gráficos de terceiros no kit de mídia Windows ou "In Box".
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b1703210318f55dad3e50f4dcdd7e143434275b7ef3b41203f41792262a53e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882706"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migração de driver gráfico para Windows 10

Windows 10 A mídia Windows 10, como seu antecessor, Windows 8.1, não tem drivers gráficos de terceiros no kit de mídia Windows ou "In Box". Em vez disso, os drivers gráficos para uma ampla gama de dispositivos são provisionados no WU, o que permite que os fornecedores de hardware atualizem drivers sem exigir uma alteração na imagem do sistema operacional. Além disso, os drivers existentes não são migrados para Windows 10 durante uma atualização do sistema operacional para Windows 10 do Windows 7, Windows 8 ou Windows 8.1. Isso também afeta as atualizações do Windows Server 2012.

## <a name="upgrades-and-installation"></a>Atualizações e instalação

Para atualizações e novas instalações, os drivers gráficos devem ser obtidos do WU (atualização Windows) ou do site IHV/OEM para o hardware relevante. Isso requer uma conexão à Internet. Os drivers no WU são injetados na configuração do sistema operacional pela DU (Atualização Dinâmica) quando um usuário atualiza seu sistema Windows 7 ou Windows 8.x para Windows 10.

> [!Note]  
> Isso não se aplica a sistemas que vêm com Windows pré-instalados, por exemplo, computadores fora da plataforma adquiridos em uma loja de varejo. Esses sistemas já têm os drivers gráficos instalados pelo OEM. O OEM também pode fornecer um DVD (para instalar o sistema operacional) que inclui os drivers.

 

Depois de atualizar para Windows 10, os usuários podem descobrir que não há drivers gráficos instalados em seu computador. Isso pode ocorrer por alguns motivos:

-   O usuário se elegeu para fazer uma instalação limpa, ou seja, não uma atualização.
-   O usuário desleixou a opção de verificar se há atualizações durante a atualização, ou seja, desabilitou efetivamente a DU (Atualização Dinâmica).
-   A conexão com a Internet não estava funcionando durante a atualização.
-   Falha na instalação do driver.

Após uma instalação limpa do sistema operacional, não haverá drivers gráficos no computador até que o cliente WU seja executado automaticamente e baixe os drivers aplicáveis. Nesse ínterim, o pc executará o MSBDA (Microsoft Basic Display Adapter), que tem funcionalidades limitadas, por exemplo, sem suporte para vários monitores e o usuário também poderá ter um desempenho ruim em comparação com um driver de hardware, por exemplo, taxa de quadros lenta ou danos na reprodução de vídeo.

## <a name="manifestations"></a>Manifestações

Para PCs mais antigos (normalmente construídos antes do Windows 7), é possível que não haja drivers para Windows 10 no WU porque os adaptadores gráficos atingiram o EOL (Fim da Vida Útil) e não têm mais suporte dos fornecedores de hardware. Até mesmo sistemas que executam o Windows 7 ou 8.x podem ter sido atualizados de um sistema operacional anterior e podem ter adaptadores gráficos EOL.

PCs mais novos podem não ter drivers disponíveis porque o adaptador gráfico foi transferido de um computador mais antigo, por exemplo, durante uma atualização de hardware. Isso geralmente acontece para computadores com vários adaptadores gráficos em que o usuário mantém uma placa gráfica antiga ao comprar um novo computador para usar várias exibições.

Outra possibilidade para um pequeno percentual de máquinas é que Windows Update tenha apenas drivers de "cobertura". Esses são drivers genéricos que não têm personalizações OEM. Um usuário que é entregue a um desses drivers após a atualização para Windows 10 pode ver que algumas funcionalidades estão ausentes, por exemplo, chaves de função para controlar o brilho da tela não funcionam mais.

## <a name="mitigations"></a>Atenuações

-   Drivers gráficos adequados devem ser entregues pelo DU durante o processo de atualização ou pelo WU logo após a conclusão da atualização. Os OEMs devem garantir que os drivers gráficos apropriados sejam incluídos nas imagens do sistema usadas para a instalação de fábrica Windows 10 em seus computadores.
-   Após uma atualização, o usuário pode verificar explicitamente Configurações Windows Atualizar para drivers, embora \\ isso não deva ser necessário. Os usuários que forçam uma verificação enquanto um driver está sendo instalado automaticamente em segundo plano poderão ver uma falha na instalação do driver se a instalação automática for concluída primeiro. Ela pode ser ignorada.
-   Os usuários que pretendem fazer uma instalação limpa do Windows 10 devem obter os drivers relevantes antes de instalar ou contar com a atualização do Windows para fornecer os drivers posteriormente, nesse caso, eles devem garantir que sua conexão com a Internet está funcionando.
-   Para computadores que recebem um driver de cobertura, não há mitigação para a funcionalidade ausente. No entanto, isso só deve acontecer em casos em que o fornecedor de hardware não mantém mais os drivers, ou seja, computadores com vários anos de idade.

> [!Note]  
> Para sistemas com uma única exibição, por exemplo, um laptop, muitos usuários acham que o MSBDA é aceitável e não notam a falta de um driver de hardware. Nenhuma mitigação é necessária nesse caso.

 

## <a name="solutions"></a>Soluções

É essencial que IHVs e OEMs carreguem seus drivers Windows 10 gráficos para WU para qualquer hardware que eles pretendam dar suporte.

Os usuários devem deixar a opção "Verificar atualizações" selecionada (a configuração padrão) ao atualizar. Dependendo da velocidade da conexão de rede e da carga nos servidores WU, isso pode significar que os drivers não serão instalados até que o OOBE seja concluído e o usuário tenha feito logon pela primeira vez. Enquanto isso, o usuário pode observar algumas funcionalidades limitadas ou desempenho ruim.

Os usuários devem garantir que sua conexão com a Internet está funcionando antes de iniciar uma atualização, mesmo que eles sejam atualizados usando mídia (DVD ou Unidade Flash).

-   Se o computador estiver conectado à Internet, os drivers apropriados deverão ser baixados e instalados automaticamente. O usuário não precisa tomar nenhuma ação.
-   Se o computador não estiver conectado à Internet, os drivers deverão ser baixados do site IHV ou OEM usando um computador conectado à Internet; transferido para o computador de destino usando uma Unidade Flash ou CD/DVD; e, em seguida, instalado manualmente.

 

 




