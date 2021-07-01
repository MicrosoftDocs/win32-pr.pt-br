---
description: Saiba como usar parâmetros em um documento PrintCapabilities. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Usando parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6417a6d30716cf19d22773c28dbf471e75f967d6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119391"
---
# <a name="using-parameters"></a>Usando parâmetros

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Além de pontuar corretamente uma Opção que contém instâncias ParameterRef (consulte [Parâmetros](referencing-parameters.md)de Referência), os provedores e clientes PrintCapabilities ou PrintTicket devem estar preparados para lidar com as seguintes situações que envolvem parâmetros.

Os clientes da interface do usuário devem solicitar que o usuário forneça inicializadores de parâmetro (valores para elementos ParameterInit) para parâmetros designados no momento apropriado para que os elementos ParameterInit apropriados sejam inseridos no PrintTicket. Os clientes de interface do usuário devem ser capazes de distinguir os dois tipos de parâmetros, incondicionalmente obrigatórios e condicionalmente obrigatórios, e devem ser capazes de lidar com cada tipo adequadamente. Para um parâmetro incondicionalmente obrigatório, a interface do usuário deve garantir que um elemento ParameterInit seja fornecido para esse tipo de parâmetro. Para um parâmetro condicionalmente obrigatório, a interface do usuário deverá fornecer um valor ParameterInit se o parâmetro for referenciado por uma Opção selecionada no PrintTicket. O status obrigatório de um parâmetro é especificado em uma instância parameterDef. Para obter mais informações, [consulte ParameterDef e ParameterInit Elements](parameterdef-and-parameterinit-elements.md). Os clientes de interface do usuário devem validar os valores ParameterInit fornecidos pelo usuário para verificar se atendem aos requisitos especificados na instância parameterDef.

Os provedores PrintTicket também devem verificar as instâncias ParameterInit fornecidas pelo PrintTicket para verificar se todos os parâmetros necessários estão presentes e se eles atendem aos requisitos especificados na instância parameterDef. O código de validação deve fornecer padrões razoáveis caso os valores parameterInit sejam inválidos ou ausentes. Observe que um ParameterDef permite que um valor padrão seja fornecido para essa finalidade. Além disso, se houver restrições envolvendo os parâmetros, por exemplo, "se *CopyCount* for maior que N, não use um compartimento de entrada de capacidade pequena", o código de validação printTicket deverá detectar essa restrição e modificar o PrintTicket para evitar ativar a restrição.

Se houver alguma dependência do PrintCapabilities nos parâmetros especificados no PrintTicket, os provedores printCapabilities deverão monitorar os valores parameterInit e produzir um documento PrintCapabilities apropriado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



