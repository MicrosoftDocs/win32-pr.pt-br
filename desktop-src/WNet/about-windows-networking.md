---
title: Sobre a rede do Windows
description: Os aplicativos podem usar as funções WNet para adicionar e cancelar conexões de rede e para recuperar informações sobre a configuração atual da rede.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- WNet de rede do Windows, descrito
- WNet WNet, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006124"
---
# <a name="about-windows-networking"></a>Sobre a rede do Windows

Os aplicativos podem usar as funções WNet para adicionar e cancelar conexões de rede e para recuperar informações sobre a configuração atual da rede.

A figura a seguir mostra a estrutura de uma rede típica.

![estrutura de rede típica](images/csnet-01.png)

Na figura anterior, a hierarquia dos recursos do Windows NT Server/Windows 2000 Server é fornecida em detalhes como o provedor de rede \# 1. Os recursos de rede de outros provedores têm diferentes sistemas hierárquicos. Um aplicativo não precisa de informações sobre a hierarquia antes de começar a trabalhar com uma rede. Ele pode prosseguir da raiz de rede (ou seja, o mais alto recurso de contêiner) e recuperar informações sobre os recursos da rede, pois as informações são necessárias.

Os recursos de rede que contêm outros recursos são chamados *contêineres*. Os recursos de contêiner estão em caixas na figura anterior.

Os recursos que não contêm outros recursos são chamados de *objetos*. Na figura anterior, o SharePoint \# 1 e o SharePoint \# 2 são objetos. Um *SharePoint* é um objeto que pode ser acessado pela rede. Exemplos de SharePoints incluem impressoras e diretórios compartilhados.

 

 




