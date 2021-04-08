---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Restrições e validação de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddcc1f6f3ad496b6bfb6ed201cf93c2b4a10679
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930236"
---
# <a name="constraints-and-printticket-validation"></a>Restrições e validação de PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Conforme discutido na seção de esquema PrintCapabilities, alguns dos resultados de configuração possíveis expressos em um documento PrintCapabilities são inválidos para o dispositivo. As configurações que são inválidas devem conter conflitos de restrição (um termo usado no mundo dos arquivos PPD/GPD). Para evitar conflitos de restrição, os provedores de PrintTicket devem dar suporte a uma operação de validação de PrintTicket que os clientes usam para executar a validação em seu PrintTicket. Esta operação deve detectar se a configuração especificada pode ocorrer no dispositivo. Se a configuração não puder ocorrer (porque os elementos de recurso e opção especificados não existem no dispositivo atual ou porque a configuração está restrita), a operação deverá modificar o PrintTicket de entrada para que ele contenha configurações válidas e não restringidas. A operação também pode remover ou validar outras informações no PrintTicket. Observe que quando um conflito de restrição é encontrado, o código de validação deve alterar a configuração de um dos atributos do dispositivo para evitar o conflito de restrição. As [definições de opção](option-definitions.md) sugerem que um processo de Pontuação definido pelo driver de dispositivo deve ser usado para determinar qual atributo de dispositivo deve ser alterado para preservar melhor a intenção original do usuário. O código de validação pode codificar o processo de Pontuação para favorecer um atributo de dispositivo sobre outro ou pode usar informações fornecidas por uma instância de propriedade específica no PrintTicket para orientar a resolução. Como não há nenhuma propriedade definida nas palavras-chave do esquema de impressão que permite aos clientes especificar a prioridade relativa de cada atributo de dispositivo, qualquer elemento de Propriedade PrintTicket particular usado para essa finalidade provavelmente será ignorado por outros provedores de PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



