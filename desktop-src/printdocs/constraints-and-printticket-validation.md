---
description: Para evitar conflitos de restrição, os provedores PrintTicket devem dar suporte à validação que os clientes usam para executar a validação em seu PrintTicket.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Restrições e validação printTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08abc07f0ef96e94720f8f9431a192e5dbcac669
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409569"
---
# <a name="constraints-and-printticket-validation"></a>Restrições e validação printTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Conforme discutido na seção Esquema PrintCapabilities, alguns dos possíveis resultados de configuração expressos em um documento PrintCapabilities são inválidos para o dispositivo. As configurações inválidas devem conter conflitos de restrição (um termo usado no mundo dos arquivos PPD/GPD). Para evitar conflitos de restrição, os provedores PrintTicket devem dar suporte a uma operação de validação PrintTicket que os clientes usam para executar a validação em seu PrintTicket. Essa operação deve detectar se a configuração especificada pode ocorrer no dispositivo. Se a configuração não puder ocorrer (porque os elementos Recurso e Opção especificados não existem no dispositivo atual ou porque a configuração está restrita), a operação deverá modificar o PrintTicket de entrada para que ele contenha configurações válidas e não restritas. A operação também pode remover ou validar outras informações no PrintTicket. Observe que, quando um conflito de restrição é encontrado, o código de validação deve alterar a configuração de um dos atributos do dispositivo para evitar o conflito de restrição. [As definições de](option-definitions.md) opção sugerem que um processo de pontuação definido pelo driver de dispositivo deve ser usado para determinar qual atributo de dispositivo deve ser alterado para preservar melhor a intenção original do usuário. O código de validação pode codificar o processo de pontuação para favorecer um atributo de dispositivo em vez de outro ou pode usar informações fornecidas por uma instância de Propriedade específica no PrintTicket para orientar a resolução. Como não há nenhuma Propriedade definida nas Palavras-chave de esquema de impressão que permita que os clientes especifiquem a prioridade relativa de cada atributo de dispositivo, qualquer elemento de Propriedade PrintTicket privado usado para essa finalidade provavelmente será ignorado por outros provedores PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



