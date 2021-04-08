---
description: Uma página de referência de evento (ERP) é um documento HTML que fornece Monitor de Rede informações sobre os eventos detectados durante a operação de monitor ou especialista.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Sobre páginas de referência de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828564"
---
# <a name="about-event-reference-pages"></a>Sobre páginas de referência de evento

Uma página de referência de evento (ERP) é um documento HTML que fornece Monitor de Rede informações sobre os eventos detectados durante a operação de monitor ou especialista.

Você pode exibir ERPs na Visualizador de Eventos de Monitor de Rede, monitorar ferramenta de controle ou em qualquer navegador que ofereça suporte aos recursos HTML do Microsoft Internet Explorer versão 4, 1 ou posterior. Ou seja, você pode adicionar controles com suporte ou linguagens com script em seu ERP.

No entanto, ERPs só aparecerá se o especialista designar o documento HTML por nome. Quando indicado corretamente, o ERP aparece no painel inferior quando o evento na Visualizador de Eventos é selecionado. A figura a seguir mostra um ERP associado ao monitor de intervalo de IP (Internet Protocol).

![um ERP associado ao monitor de intervalo de IP](images/exview2.png)

## <a name="expert-events"></a>Eventos de especialistas

Os eventos de especialista são identificados pelo membro **EventIdent** de uma estrutura [**NMEVENTDATA**](nmeventdata.md) . Ao escrever um especialista, você determina os valores de **EventIdent** , que normalmente são numerados 1, 2, 3 e assim por diante. Por exemplo, suponha que um especialista gere dois eventos (**EventIdent1** e **EventIdent2**). Se você quiser que o Visualizador de Eventos exiba os eventos separadamente, você deve criar dois documentos ERP separados.

 

 



