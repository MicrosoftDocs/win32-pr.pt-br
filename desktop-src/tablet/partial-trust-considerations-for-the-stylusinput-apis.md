---
description: Visão geral dos problemas de confiança parcial e da API (interface de programação de aplicativo) do StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Considerações de confiança parcial para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170691"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Considerações de confiança parcial para a API StylusInput

O [**RealTimeStylus**](realtimestylus-class.md) que usa o *parâmetro Handle* requer as permissões [UIPermissionWindow. @ Windows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) , além das permissões exigidas pelo construtor que usa o parâmetro *attachedControl* .

Para obter mais informações sobre problemas de segurança e confiança, consulte [segurança e confiança](security-and-trust.md).

 

 
