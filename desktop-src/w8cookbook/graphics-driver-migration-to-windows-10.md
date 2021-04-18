---
title: Migração de driver de gráficos para o Windows 10
description: O Windows 10 Media e o Windows 10, como seu antecessor, Windows 8.1, não têm nenhum driver gráfico de terceiros no Windows Media Kit ou "in box".
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a23d8ae341172223955fcc781f95b7615bcfc867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796202"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migração de driver de gráficos para o Windows 10

O Windows 10 Media e o Windows 10, como seu antecessor, Windows 8.1, não têm nenhum driver gráfico de terceiros no Windows Media Kit ou "in box". Em vez disso, os drivers gráficos para uma ampla variedade de dispositivos são provisionados no WU, o que permite que os fornecedores de hardware atualizem drivers sem exigir uma alteração na imagem do sistema operacional. Além disso, OS drivers existentes não são migrados para o Windows 10 durante uma atualização do sistema operacional para o Windows 10 do Windows 7, Windows 8 ou Windows 8.1. Isso também afeta as atualizações do Windows Server 2012.

## <a name="upgrades-and-installation"></a>Atualizações e instalação

Para atualizações e novas instalações, os drivers gráficos devem ser obtidos no Windows Update (WU) ou no site do IHV/OEM para o hardware relevante. Isso requer uma conexão à Internet. Os drivers no WU são injetados na configuração do so por atualização dinâmica (DU) quando um usuário atualiza seu sistema Windows 7 ou Windows 8. x para o Windows 10.

> [!Note]  
> Isso não se aplica a sistemas que vêm com o Windows pré-instalado, por exemplo, computadores prontos para serem comprados em uma loja de varejo. Esses sistemas já têm os drivers gráficos instalados pelo OEM. O OEM também pode fornecer um DVD (para reinstalar o sistema operacional), que inclui os drivers.

 

Após a atualização para o Windows 10, os usuários poderão descobrir que não há drivers gráficos instalados em seu PC. Isso pode ocorrer por alguns motivos:

-   O usuário optou por fazer uma instalação limpa, ou seja, não uma atualização.
-   O usuário desselecionou a opção de verificar se há atualizações durante a atualização, ou seja, desabilitada efetivamente a atualização dinâmica (DU).
-   A conexão com a Internet não estava funcionando durante a atualização.
-   Falha na instalação do driver.

Após uma instalação limpa do sistema operacional, não haverá nenhum driver de gráficos no computador até que o cliente WU seja executado automaticamente e baixe os drivers aplicáveis. No interim, o PC executará o adaptador de vídeo básico da Microsoft (MSBDA), que tem recursos limitados, por exemplo, não há suporte para vários monitores, e o usuário também pode experimentar um desempenho insatisfatório em comparação com um driver de hardware, por exemplo, taxa de quadros lenta ou contornar a reprodução de vídeo.

## <a name="manifestations"></a>Manifestações

Para PCs mais antigos (normalmente criados antes do Windows 7), é possível que não haja drivers para o Windows 10 no WU porque os adaptadores gráficos chegaram ao fim da vida útil (EOL) e não têm mais suporte dos fornecedores de hardware. Mesmo OS sistemas que atualmente executam o Windows 7 ou 8. x podem ter sido atualizados de um sistema operacional anterior e ter adaptadores de gráficos de EOL.

Computadores mais novos podem não ter drivers disponíveis porque o adaptador gráfico foi transferido de um computador mais antigo, por exemplo, durante uma atualização de hardware. Isso geralmente acontece com computadores com vários adaptadores gráficos em que o usuário manteve uma placa gráfica antiga ao comprar um novo computador para usar vários monitores.

Outra possibilidade de um pequeno percentual de computadores é que Windows Update tem apenas drivers de "cobertura". Esses são drivers genéricos que não têm personalizações de OEM. Um usuário que entrega um desses drivers após a atualização para o Windows 10 pode ver que alguma funcionalidade está ausente, por exemplo, as teclas de função para controlar o brilho da tela não funcionam mais.

## <a name="mitigations"></a>Atenuações

-   Os drivers gráficos adequados devem ser entregues pelo DU durante o processo de atualização ou pelo WU logo após a conclusão da atualização. Os OEMs devem garantir que os drivers gráficos apropriados sejam incluídos nas imagens do sistema usadas para a instalação de fábrica do Windows 10 em seus computadores.
-   Após uma atualização, o usuário pode verificar explicitamente as configurações \\ Windows Update para drivers, embora isso não seja necessário. Os usuários que forçam uma verificação enquanto um driver está sendo instalado automaticamente em segundo plano podem ver uma falha de instalação do driver se a instalação automática for concluída primeiro. Ela pode ser ignorada.
-   Os usuários que pretendem fazer uma instalação limpa do Windows 10 devem obter os drivers relevantes antes de instalar ou contar com Windows Update para fornecer os drivers mais tarde, caso em que eles devem garantir que a conexão com a Internet esteja funcionando.
-   Para computadores que recebem um driver de cobertura, não há nenhuma mitigação para a funcionalidade ausente. No entanto, isso só deve acontecer em casos em que o fornecedor de hardware não mantém mais os drivers, ou seja, computadores com vários anos de idade.

> [!Note]  
> Para sistemas com uma única exibição, por exemplo, um laptop, muitos usuários acham que o MSBDA é aceitável e não observa a falta de um driver de hardware. Nesse caso, nenhuma mitigação é necessária.

 

## <a name="solutions"></a>Soluções

É fundamental que os IHVs e os OEMs Carreguem seus drivers gráficos do Windows 10 no WU para qualquer hardware ao qual pretendem dar suporte.

Os usuários devem deixar a opção "verificar atualizações" selecionada (a configuração padrão) ao atualizar. Dependendo da velocidade da conexão de rede e da carga nos servidores do WU, isso pode significar que os drivers não são instalados até que o OOBE seja concluído e o usuário tenha feito o logon pela primeira vez. Enquanto isso, o usuário pode observar alguma funcionalidade limitada ou baixo desempenho.

Os usuários devem garantir que sua conexão com a Internet esteja funcionando antes de iniciar uma atualização, mesmo se estiverem atualizando usando mídia (unidade flash ou DVD).

-   Se o PC estiver conectado à Internet, os drivers apropriados deverão ser baixados e instalados automaticamente. O usuário não precisa realizar nenhuma ação.
-   Se o PC não estiver conectado à Internet, os drivers deverão ser baixados do site do IHV ou OEM usando um computador conectado à Internet; transferido para o computador de destino usando uma unidade flash ou CD/DVD; e, em seguida, instalado manualmente.

 

 




