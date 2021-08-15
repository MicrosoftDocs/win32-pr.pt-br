---
description: Remoção de WPDUSB.SYS driver para Windows portáteis
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Remoção de WPDUSB.SYS driver para Windows portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b5d1a815b97049816a618b9e93d0767e321fd60b689e6845318c1605574c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994736"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Remoção de WPDUSB.SYS driver para Windows portáteis

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Gravidade –** Baixa  
**Frequência** – Baixa  





## <a name="description"></a>Descrição

A Microsoft substituiu o componente de modo kernel da pilha de driver USB (WPDUSB.SYS) do Windows Vista para wpd (dispositivos portáteis) Windows pelo driver WINUSB.SYS genérico. A comunicação com o driver WPDUSB.SYS original ocorreu por meio de códigos de IOCTL (Controle de E/S privado); O suporte a eles também foi removido.

Qualquer consumidor desses códigos IOCTL seria responsável pela interpretação e implementação adequadas do protocolo MTP. Windows O Vista não deu suporte ao uso desses códigos IOCTL por aplicativos de terceiros.

## <a name="manifestation-of-impact"></a>Manifestação de impacto

Qualquer aplicativo que dependesse da disponibilidade desses códigos IOCTL privados não teria mais acesso a dispositivos MTP conectados por USB.

## <a name="mitigation"></a>Atenuação

Os usuários de um aplicativo que depende dos códigos IOCTL privados devem usar um aplicativo diferente (ou uma versão atualizada do aplicativo) para acessar o dispositivo MTP conectado por USB.

## <a name="solution"></a>Solução

Os aplicativos devem usar a API Windows WPD (Dispositivos Portáteis) para encontrar e interagir com qualquer dispositivo WPD. Embora uma porcentagem significativa de dispositivos WPD implemente o MTP para comunicação com o computador, o WPD não está limitado apenas a dispositivos MTP. Além disso, em que o acesso direto ao dispositivo por meio das IOCTLs privadas limitaria o aplicativo à comunicação apenas com dispositivos conectados por USB, o uso da API WPD expande a lista de opções de conectividade para outros protocolos de comunicação (por exemplo, Wi-Fi). Nos casos raros em que o aplicativo deve estar ciente de MTP, a API WPD fornece um mecanismo de passagem para comandos MTP brutos.

## <a name="leveraging-feature-capabilities"></a>Aproveitando as funcionalidades de recursos

A API WPD tem suporte no Windows XP (por meio do SDK de formato Windows), Windows Vista e Windows 7. A Windows 7 do WPD adiciona suporte para MTP em Bluetooth.

## <a name="links-to-other-resources"></a>Links para outros recursos

[Windows Dispositivos portáteis](../windows-portable-devices.md)

 

 
