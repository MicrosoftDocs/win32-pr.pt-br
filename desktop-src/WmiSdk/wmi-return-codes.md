---
description: Esta seção fornece uma lista dos códigos de retorno WMI, constantes simbólicas, valores literais e descrições. Esses códigos podem ser retornados por scripts, aplicativos C++ ou comandos Wmic.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Códigos de retorno WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1454c8efc45085e88f78358346679b5cdcf3d05093318845912d7d5a913d8ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995376"
---
# <a name="wmi-return-codes"></a>Códigos de retorno WMI

Esta seção fornece uma lista dos códigos de retorno WMI, constantes simbólicas, valores literais e descrições. Esses códigos podem ser retornados por scripts, aplicativos C++ ou [**comandos Wmic.**](wmic.md)

Se ocorrer um erro, o WMI retornará um dos códigos de erro a seguir como um valor de 32 bits em que os dois bits de ordem alta indicam o código de severidade da mensagem.

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Êxito

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Informativo

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Aviso

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

Erro

</dd> </dl>

> [!Note]
>
> Se o WMI retornar mensagens de erro, esteja ciente de que elas podem não indicar problemas no serviço WMI ou em provedores WMI. As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI. Em qualquer circunstâncias, não exclua o repositório WMI como uma primeira ação porque a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.
>
> Para obter mais informações sobre a origem do problema, você pode baixar e executar a [Utilitário de Diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) de linha de comando de diagnóstico. Essa ferramenta produz um relatório que geralmente pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo. O relatório também ajuda os serviços de suporte da Microsoft a ajudá-lo. Você pode baixar o Utilitário de Diagnóstico WMI [aqui.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

 

-   [**Constantes de erro WMI**](wmi-error-constants.md)
-   [**Constantes sem erro WMI**](wmi-non-error-constants.md)

 

 



