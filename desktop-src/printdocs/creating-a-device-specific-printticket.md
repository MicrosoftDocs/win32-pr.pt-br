---
description: Saiba mais sobre como criar um PrintTicket específico do dispositivo, que tem como destino um dispositivo específico e é portátil em vários dispositivos.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Criando um Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b825bd875ada534c8c467cd18d90f2db9a2a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409539"
---
# <a name="creating-a-device-specific-printticket"></a>Criando um Device-Specific PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um PrintTicket específico do dispositivo tem como destino um dispositivo específico e, portanto, não é geralmente portátil em vários dispositivos.

As etapas mostradas na lista a seguir devem ser usadas quando você cria um PrintTicket específico do dispositivo.

1.  Obtenha um documento PrintCapabilities que contém apenas as instâncias de recurso relevantes para o dispositivo. Solicite um documento PrintCapabilities padrão. Isso não exige que você especifique um PrintTicket de entrada porque os atributos do dispositivo (instâncias e parâmetros de Recurso e Opção) usados para construir o PrintTicket são independentes da configuração.

2.  Crie um documento XML vazio que contém a raiz PrintTicket. Atribua um prefixo de namespace ao namespace Esquema de Impressão e atribua prefixos para todos os outros namespaces que serão usados pelo PrintTicket. Especifique a versão do esquema PrintTicket.

3.  Você pode definir configurações no PrintTicket para cada instância de Feature e ParameterDef relatada no documento PrintCapabilities ou apenas aquelas de seu interesse. Se um PrintTicket parcial for apresentado à interface PrintTicket, os padrões serão fornecidos automaticamente para instâncias de Feature e ParameterDef omitidas durante a validação de PrintTicket.

4.  Examine o documento PrintCapabilities para Instâncias de recurso e determine quais delas você deseja definir em seu PrintTicket. Adicione essas instâncias de recurso ao PrintTicket, mas não transfira o conteúdo das instâncias de recurso para o PrintTicket. Se você transferir uma subfeature, o Recurso pai também deverá ser transferido e a relação pai-filho deverá ser preservada no PrintTicket.

    Para cada Recurso que você transferir, determine quais instâncias de Opção são aplicáveis ao PrintTicket. Transfira a Opção inteira conforme definido no documento PrintCapabilities e remova todas as instâncias de Propriedade presentes. As instâncias de Propriedade são usadas em documentos PrintCapabilities, mas não servem para nenhuma finalidade no PrintTicket. Mantenha todas as instâncias ScoredProperty, certifique-se de preservar sua localização; eles são uma parte intrínseca da definição de Opção.

5.  Você também pode adicionar Instâncias de propriedade a qualquer instância ScoredProperty. As instâncias de propriedade serão usadas somente se o provedor PrintTicket for explicitamente compatível com seu uso. Cada provedor deve documentar a finalidade e o uso de todas as instâncias de Propriedade com suporte. Observe que, durante a validação, todas as instâncias de Propriedade contidas em uma instância option são retiradas, a menos que o namespace da Propriedade seja reconhecido pelo provedor PrintCapabilities ou PrintTicket de destino e uma Opção candidata seja encontrada no documento PrintCapabilities cujas instâncias ScoredProperty corresponderão perfeitamente às definidas na Opção de referência.

6.  Se as Palavras-chave de esquema de impressão definirem a propriedade SelectionType como PickMany para um recurso específico, você poderá selecionar mais de uma Opção para esse Recurso, desde que a Opção designada como IdentityOption não seja uma das selecionadas. IdentityOption no Esquema de Impressão tem o mesmo efeito que a opção None em arquivos POSTSCRIPT PPD e arquivos GPD Unidrv; ele serve como uma não operação.

7.  Examine o documento PrintCapabilities para instâncias ParameterDef que devem ser definidas em seu PrintTicket. Para cada instância parameterDef, selecione um Valor a ser usado na instância ParameterInit no PrintTicket. Esse Valor deve ser do tipo de dados correto e deve estar dentro do intervalo definido na instância parameterDef e deve atender a todos os outros requisitos especificados na instância parameterDef. Use uma instância ParameterInit para inicializar o parâmetro para o Valor selecionado.

8.  Examine o conteúdo de cada instância option que aparece no PrintTicket para ocorrências de instâncias ParameterRef. Se uma instância parameterInit correspondente ainda não aparecer no PrintTicket, siga a etapa anterior para criar uma instância ParameterInit no PrintTicket. A finalidade dessa instância ParameterInit é inicializar o parâmetro referenciado pela instância ParameterRef.

9.  Tenha em mente que conflitos de restrição podem impedir que o dispositivo aplica a configuração especificada no PrintTicket. Se necessário, o processo de validação modifica a configuração definida no PrintTicket para uma que está livre de conflitos.

10. Examine as Palavras-chave de esquema de impressão para instâncias de propriedade que devem estar presentes em seu PrintTicket. Adicione uma instância property ao PrintTicket para cada que for necessário e forneça um valor adequado para ela usando o tipo de elemento Value. Certifique-se de que as instâncias de Propriedade estão localizadas corretamente dentro do PrintTicket.

11. Examine as instâncias de Propriedade opcionais no esquema PrintTicket. Se houver essas instâncias de Propriedade que devem estar em seu PrintTicket, crie-as em seu PrintTicket.

12. Você também pode adicionar instâncias de Propriedade definidas de forma privada no nível raiz ou a qualquer instância de Recurso, Opção ou Propriedade. Observe, no entanto, que essas instâncias de Propriedade definidas de forma privada são retiradas durante a validação, a menos que o namespace ao que pertencem seja reconhecido pelo provedor PrintCapabilities ou PrintTicket de destino. Além disso, as instâncias de propriedade que aparecem em qualquer lugar dentro de uma instância option são retiradas durante a validação, a menos que o documento PrintCapabilities contenha uma Opção que seja uma combinação perfeita. Duas instâncias option serão uma combinação perfeita se cada ScoredProperty em uma instância option tiver uma ScoredProperty correspondente na outra e os Valores das instâncias ScoredProperty são os mesmos. Consulte o Esquema Privado do provedor PrintTicket para ver uma lista de instâncias de propriedade privada reconhecidas e seus usos.

13. Os filhos do mesmo tipo de elemento podem não aninhar a uma profundidade de mais de 10 elementos. Essa regra se aplica independentemente a cada tipo de elemento que pode ser definido.

> [!Note]  
> O conteúdo XML printTicket DEVE ser codificado usando UTF-8 ou UTF-16.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



