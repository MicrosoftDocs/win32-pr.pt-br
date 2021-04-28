---
description: Remoção do driver de WPDUSB.SYS para dispositivos portáteis do Windows
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Remoção do driver de WPDUSB.SYS para dispositivos portáteis do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116244"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Remoção do driver de WPDUSB.SYS para dispositivos portáteis do Windows

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

A Microsoft substituiu o componente de modo kernel da pilha de drivers USB do Windows Vista (WPDUSB.SYS) para dispositivos portáteis do Windows (WPD) pelo driver WINUSB.SYS genérico. A comunicação com o driver de WPDUSB.SYS original era por meio de códigos de controle de e/s privada (IOCTL); o suporte deles também foi removido.

Qualquer consumidor desses códigos de IOCTL teria sido responsável por uma interpretação adequada e a implementação do MTP (protocolo de transferência de mídia). O Windows Vista não oferecia suporte ao uso desses códigos de IOCTL por aplicativos de terceiros.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Qualquer aplicativo que dependa da disponibilidade desses códigos de IOCTL privado não teria mais acesso a dispositivos MTP conectados por USB.

## <a name="mitigation"></a>Atenuação

Os usuários de um aplicativo que depende dos códigos de IOCTL privados devem usar um aplicativo diferente (ou uma versão atualizada do aplicativo) para acessar o dispositivo MTP conectado por USB.

## <a name="solution"></a>Solução

Os aplicativos devem usar a API de dispositivos portáteis do Windows (WPD) para localizar e interagir com qualquer dispositivo WPD. Embora uma porcentagem significativa de dispositivos WPD implemente MTP para comunicação com o PC, o WPD não se limita apenas a dispositivos MTP. Além disso, em que o acesso direto ao dispositivo por meio de IOCTLs privados teria limitado o aplicativo de comunicação apenas com dispositivos conectados por USB, o uso da API WPD expande a lista de opções de conectividade para outros protocolos de comunicação (por exemplo, Wi-Fi). Nos casos raros em que o aplicativo deve ser compatível com MTP, a API WPD fornece um mecanismo de passagem para comandos do MTP brutos.

## <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

A API WPD tem suporte no Windows XP (por meio do Windows Format SDK), do Windows Vista e do Windows 7. A implementação do Windows 7 de WPD adiciona suporte para MTP em Bluetooth.

## <a name="links-to-other-resources"></a>Links para outros recursos

[Dispositivos portáteis do Windows](../windows-portable-devices.md)

 

 
