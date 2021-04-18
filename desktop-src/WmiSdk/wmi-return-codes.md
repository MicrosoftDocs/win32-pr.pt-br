---
description: Esta seção fornece uma lista dos códigos de retorno do WMI, constantes simbólicas, valores literais e descrições. Esses códigos podem ser retornados por scripts, aplicativos C++ ou comandos WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Códigos de retorno do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781200"
---
# <a name="wmi-return-codes"></a>Códigos de retorno do WMI

Esta seção fornece uma lista dos códigos de retorno do WMI, constantes simbólicas, valores literais e descrições. Esses códigos podem ser retornados por scripts, aplicativos C++ ou comandos [**WMIC**](wmic.md) .

Se ocorrer um erro, o WMI retornará um dos seguintes códigos de erro como um valor de 32 bits, em que os dois bits de ordem superior indicam o código de severidade da mensagem.

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

<span id="3"></span>Beta
</dt> <dd>

Erro

</dd> </dl>

> [!Note]
>
> Se o WMI retornar mensagens de erro, lembre-se de que eles podem não indicar problemas no serviço WMI ou em provedores WMI. As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI. Em qualquer circunstância, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.
>
> Para obter mais informações sobre a origem do problema, você pode baixar e executar a ferramenta de linha de comando de diagnóstico [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) . Essa ferramenta produz um relatório que, em geral, pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo. O relatório também ajuda os serviços de suporte da Microsoft para ajudá-lo. Você pode baixar o Utilitário de Diagnóstico WMI [aqui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

-   [**Constantes de erro WMI**](wmi-error-constants.md)
-   [**Constantes de não erro do WMI**](wmi-non-error-constants.md)

 

 



