---
description: A referência de script do WMI contém definições para a API de script do WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de script para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827729"
---
# <a name="scripting-api-for-wmi"></a>API de script para WMI

A referência de script do WMI contém definições para a API de script do WMI. Use essa API se estiver escrevendo aplicativos com o Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript) ou qualquer outra linguagem de script que ofereça suporte a tecnologias de script ativas.

> [!Note]  
> O PowerShell também está disponível para scripts com o WMI. O cmdlet Get-WMI e os três aceleradores de tipo ( \[ WMI \] , \[ WMIClass \] e \[ WMISEARCHER \] ) habilitam o acesso administrativo básico ao WMI. Para obter mais informações, consulte [scripts com o Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Os objetos de script WMI, exceto para [**SWbemDateTime**](swbemdatetime.md) , não são marcados como seguros para scripts em execução em páginas HTML no Internet Explorer. Portanto, a menos que o nível de segurança no Internet Explorer seja reduzido, o script falhará. **SWbemDateTime** é marcado como seguro para inicialização e scripts. No entanto, use todos os objetos de script WMI em chamadas **GetObject** e **CreateObject** no código do lado do servidor em páginas do Active Server (ASP).

-   [Modelo de objeto de API de script](scripting-api-object-model.md)
-   [Convenções de documento para a API de script](document-conventions-for-the-scripting-api.md)
-   [Objetos de API de script](scripting-api-objects.md)
-   [Constantes de API de script](scripting-api-constants.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de WMI](wmi-reference.md)
</dt> <dt>

[Códigos de retorno do WMI](wmi-return-codes.md)
</dt> </dl>

 

 



