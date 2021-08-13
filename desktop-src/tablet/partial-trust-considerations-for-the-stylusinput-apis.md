---
description: Visão geral dos problemas de confiança parcial e da API (interface de programação de aplicativo) StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Considerações de confiança parcial para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 596e8b50692ae09e9fbaf73f9254afbec8f29d6481a2dc3e27727beb27546441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449346"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Considerações de confiança parcial para a API StylusInput

A [**RealTimeStylus**](realtimestylus-class.md) que  assume o parâmetro handle requer as permissões [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag.UnmanagedCode,](/previous-versions/windows/) além das permissões exigidas pelo construtor que leva o parâmetro *attachedControl.*

Para obter mais informações sobre problemas de segurança e confiança, consulte [Segurança e confiança.](security-and-trust.md)

 

 
