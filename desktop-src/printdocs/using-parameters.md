---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Usando parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fe8fc7c79ed27c467b59ef67132e816cdcd63
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172551"
---
# <a name="using-parameters"></a>Usando parâmetros

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Além de apresentar corretamente uma opção que contém instâncias ParameterRef (consulte [parâmetros de referência](referencing-parameters.md)), os provedores de PrintCapabilities ou PrintTicket e os clientes devem estar preparados para lidar com as seguintes situações envolvendo parâmetros.

Os clientes da interface do usuário (IU) devem solicitar que o usuário forneça inicializadores de parâmetro (valores para elementos ParameterInit) para os parâmetros designados no momento apropriado para que os elementos ParameterInit apropriados sejam inseridos no PrintTicket. Os clientes da interface do usuário devem ser capazes de distinguir os dois tipos de parâmetros, incondicionalmente obrigatórios e condicionalmente obrigatórios, e devem ser capazes de lidar com cada tipo adequadamente. Para um parâmetro obrigatório incondicionalmente, a interface do usuário deve garantir que um elemento ParameterInit seja fornecido para esse tipo de parâmetro. Para um parâmetro condicionalmente obrigatório, a interface do usuário deve fornecer um valor ParameterInit se o parâmetro for referenciado por uma opção selecionada no PrintTicket. O status obrigatório de um parâmetro é especificado em uma instância de ParameterDef. Para obter mais informações, consulte [elementos ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md). Os clientes da interface do usuário devem validar os valores de ParameterInit fornecidos pelo usuário para verificar se eles atendem aos requisitos especificados na instância do ParameterDef.

Os provedores PrintTicket também devem verificar as instâncias de ParameterInit fornecidas pelo PrintTicket para verificar se todos os parâmetros necessários estão presentes e se eles atendem aos requisitos especificados na instância ParameterDef. O código de validação deve fornecer padrões razoáveis caso os valores de ParameterInit sejam inválidos ou ausentes. Observe que um ParameterDef permite que um valor padrão seja fornecido para essa finalidade. Além disso, se houver restrições envolvendo os parâmetros, por exemplo, "se *CopyCount* for maior que N, não usar uma bandeja de entrada de pequena capacidade", o código de validação do PrintTicket deverá detectar essa restrição e modificar o PrintTicket para evitar a ativação da restrição.

Se houver qualquer dependência das PrintCapabilities nos parâmetros especificados no PrintTicket, os provedores de PrintCapabilities deverão monitorar os valores de ParameterInit e produzir um documento de PrintCapabilities adequado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



