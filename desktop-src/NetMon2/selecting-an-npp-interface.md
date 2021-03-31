---
description: Os NPPs (provedores de pacotes de rede) expõem as interfaces IDelaydC, IESP, IRTC e IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Selecionando uma interface NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827859"
---
# <a name="selecting-an-npp-interface"></a>Selecionando uma interface NPP

Os NPPs (provedores de pacotes de rede) expõem as interfaces [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md)e [**IStats**](istats.md) . Cada uma dessas interfaces fornece métodos semelhantes para conectar o NPP à rede, capturar o tráfego de rede e coletar informações estatísticas sobre os dados capturados. Para escolher a interface a ser usada, consulte a tabela a seguir.

> [!Note]  
> Ao conectar um NPP à rede com uma dessas interfaces, você só pode usar os métodos fornecidos por essa interface. Por exemplo, se você se conectar à rede usando a interface [**IRTC**](irtc.md) e, em seguida, tentar iniciar uma captura com [**IDelaydC**](idelaydc.md), sua chamada para iniciar a captura falhará e um código de erro será retornado.

 



| Interface                    | Quando usar                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDelaydC**](idelaydc.md) | Use para capturar o tráfego de rede e armazená-lo em um arquivo de captura. Essa interface é usada pela interface do usuário do Monitor de Rede e outros aplicativos NPP, que exigem o armazenamento de informações de rede capturadas.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Usado para fornecer estatísticas aprimoradas em um formato de arquivo ESP especial. Essa interface é usada por aplicativos NPP que exigem as estatísticas aprimoradas fornecidas pelo formato ESP.<br/>                                                                                                                                                        |
| [**IRTC**](irtc.md)         | Use para capturar o tráfego de rede em tempo real e disparar eventos quando eles ocorrerem. Essa interface é usada por aplicativos NPP que exigem capturas em tempo de execução. Observe que essa interface não fornece as estatísticas que as outras interfaces NPP fornecem, nem permite que você insira quadros no tráfego de rede capturado.<br/> |
| [**IStats**](istats.md)     | Use para recuperar estatísticas de captura, mas não os quadros capturados.                                                                                                                                                                                                                                                                                 |



 

 

 




