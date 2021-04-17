---
description: Gerenciamento de esquema de energia
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Gerenciamento de esquema de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757083"
---
# <a name="power-scheme-management"></a>Gerenciamento de esquema de energia

Cada esquema de energia é identificado exclusivamente por um **GUID**. Para enumerar todos os esquemas de energia disponíveis, use a função [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) . **PowerEnumerate** também pode ser usado para recuperar todas as configurações de energia de um esquema especificado.

O esquema de energia que está atualmente em uso no sistema é chamado de plano ou esquema de energia ativo. Para recuperar o **GUID** do plano ativo, chame a função [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) . Para alterar o plano de energia ativo, chame a função [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .

Para criar um esquema de energia, você precisa primeiro duplicar um esquema existente usando a função [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , especificando o **GUID** do esquema no qual você deseja basear seu novo esquema. Você deve copiar um dos esquemas internos e modificar as configurações de energia para suas necessidades. Observe que a criação de um plano de energia não atualiza automaticamente o plano de energia ativo. Você deve sempre chamar [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) para atualizar o plano de energia ativo. Os planos de energia existentes podem ser modificados e aplicados da mesma maneira.

Para remover um plano de energia, chame a função [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .

> [!Note]  
> Para recuperar informações adicionais sobre o estado de energia do sistema, chame a função [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquemas de energia](power-schemes.md)
</dt> </dl>

 

 



