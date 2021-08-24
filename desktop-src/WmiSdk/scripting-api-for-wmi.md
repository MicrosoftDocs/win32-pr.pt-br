---
description: A referência de script WMI contém definições para a API de Script WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de script para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35045aa8528c5a3c27475fff753478bd2202d9137cec6b019039aac52775f70a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640536"
---
# <a name="scripting-api-for-wmi"></a>API de script para WMI

A referência de script WMI contém definições para a API de Script WMI. Use essa API se estiver escrevendo aplicativos com o Microsoft Visual Basic, Visual Basic for Applications, Visual Basic VBScript (Scripting Edition) ou qualquer outra linguagem de script que dá suporte a tecnologias de script ativas.

> [!Note]  
> O PowerShell também está disponível para scripts com WMI. O cmdlet Get-WMI e os três aceleradores de tipo ( \[ \] wmi, \[ wmiclass e \] \[ wmisearcher ) permitem acesso administrativo \] básico ao WMI. Para obter mais informações, consulte [Scripts com Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Objetos de script WMI, exceto [**SWbemDateTime,**](swbemdatetime.md) não são marcados como seguros para scripts em execução em páginas HTML Internet Explorer. Portanto, a menos que o nível de segurança Internet Explorer seja inferior, o script falhará. **SWbemDateTime** é marcado como seguro para inicialização e script. No entanto, use todos os objetos de script WMI em **chamadas GetObject** e **CreateObject** no código do lado do servidor no ASP (Active Server Pages).

-   [Modelo de objeto da API de Script](scripting-api-object-model.md)
-   [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md)
-   [Objetos de API de script](scripting-api-objects.md)
-   [Constantes de API de script](scripting-api-constants.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de WMI](wmi-reference.md)
</dt> <dt>

[Códigos de retorno WMI](wmi-return-codes.md)
</dt> </dl>

 

 



