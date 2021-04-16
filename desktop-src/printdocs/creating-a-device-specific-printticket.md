---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Criando um Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31644f25f231f7121e2e492bc3f41a81b82d0b4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105782501"
---
# <a name="creating-a-device-specific-printticket"></a>Criando um Device-Specific PrintTicket

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um PrintTicket específico de dispositivo tem como alvo um dispositivo específico e, portanto, não é geralmente portável em vários dispositivos.

As etapas mostradas na lista a seguir devem ser usadas quando você cria um PrintTicket específico do dispositivo.

1.  Obtenha um documento de PrintCapabilities que contém apenas as instâncias de recurso relevantes para o dispositivo. Solicitar um documento de PrintCapabilities padrão. Isso não exige que você especifique um PrintTicket de entrada porque os atributos do dispositivo (instâncias de recurso e opção e parâmetros) que são usados para construir o PrintTicket são independentes da configuração.

2.  Crie um documento XML vazio contendo a raiz do PrintTicket. Atribua um prefixo de namespace ao namespace de esquema de impressão e atribua prefixos para todos os outros namespaces que serão usados pelo PrintTicket. Especifique a versão do esquema PrintTicket.

3.  Você pode definir configurações no PrintTicket para cada recurso e instância ParameterDef relatados no documento PrintCapabilities ou somente aqueles de seu interesse. Se um PrintTicket parcial for apresentado à interface PrintTicket, os padrões serão fornecidos automaticamente para instâncias de recurso omitido e ParameterDef durante a validação do PrintTicket.

4.  Examine o documento de PrintCapabilities em busca de instâncias de recursos e determine quais delas você deseja definir em seu PrintTicket. Adicione essas instâncias de recurso ao PrintTicket, mas não transfira o conteúdo das instâncias de recurso para o PrintTicket. Se você transferir um subrecurso, o recurso pai também deverá ser transferido e a relação pai-filho deverá ser preservada no PrintTicket.

    Para cada recurso que você transferir, determine quais instâncias de opção são aplicáveis ao seu PrintTicket. Transfira a opção inteira conforme definido no documento PrintCapabilities e, em seguida, remova as instâncias de propriedade que estão presentes. As instâncias de propriedade são usadas em documentos de PrintCapabilities, mas não servem para nenhuma finalidade no PrintTicket. Mantenha todas as instâncias de ScoredProperty, garantindo que você preserve sua localização; Eles são parte intrínseca da definição de opção.

5.  Você também pode adicionar instâncias de propriedade a qualquer instância de ScoredProperty. As instâncias de propriedade serão usadas somente se o provedor PrintTicket der suporte explicitamente ao seu uso. Cada provedor deve documentar a finalidade e o uso de todas as instâncias de propriedade com suporte. Observe que durante a validação, todas as instâncias de propriedade contidas em uma instância de opção são removidas, a menos que o namespace da propriedade seja reconhecido pelo provedor de PrintCapabilities ou PrintTicket de destino, e uma opção de candidato seja encontrada no documento de PrintCapabilities cujas instâncias ScoredProperty correspondam perfeitamente àquelas definidas na opção de referência.

6.  Se as palavras-chave do esquema de impressão definirem a Propriedade SelectionType como PickMany para um recurso específico, você poderá selecionar mais de uma opção para esse recurso, desde que a opção designada como IdentityOption não seja aquela selecionada. IdentityOption no esquema de impressão tem o mesmo efeito que a opção None em arquivos PPD PostScript e arquivos GPD do unidrv; Ele serve como um estado não operacional.

7.  Examine o documento PrintCapabilities para instâncias ParameterDef que devem ser definidas em seu PrintTicket. Para cada instância de ParameterDef, selecione um valor a ser usado na instância de ParameterInit no PrintTicket. Esse valor deve ser do tipo de dados correto e deve estar dentro do intervalo definido na instância ParameterDef e deve atender a todos os outros requisitos especificados na instância ParameterDef. Use uma instância de ParameterInit para inicializar o parâmetro para o valor que você selecionou.

8.  Examine o conteúdo de cada instância de opção que aparece no PrintTicket para ocorrências de instâncias de ParameterRef. Se uma instância ParameterInit correspondente ainda não aparecer no PrintTicket, siga a etapa anterior para criar uma instância ParameterInit no PrintTicket. A finalidade dessa instância de ParameterInit é inicializar o parâmetro referenciado pela instância ParameterRef.

9.  Tenha em mente que os conflitos de restrição podem impedir que o dispositivo aplique a configuração que você especificou no PrintTicket. Se necessário, o processo de validação modifica a configuração definida no PrintTicket para uma sem conflitos.

10. Examine as palavras-chave do esquema de impressão para as instâncias de propriedade que devem estar presentes em seu PrintTicket. Adicione uma instância de propriedade ao seu PrintTicket para cada uma delas necessária e forneça um valor adequado para ela usando o tipo de elemento de valor. Verifique se as instâncias de propriedade estão localizadas corretamente dentro do PrintTicket.

11. Examine as instâncias de propriedade opcionais no esquema PrintTicket. Se houver essas instâncias de propriedade que devem estar em seu PrintTicket, crie-as em seu PrintTicket.

12. Você também pode adicionar instâncias de propriedade definidas de modo privado no nível raiz ou a qualquer recurso, opção ou instância de propriedade. No entanto, observe que essas instâncias de propriedade definidas de forma privada são removidas durante a validação, a menos que o namespace ao qual pertencem seja reconhecido pelo provedor de PrintCapabilities ou PrintTicket de destino. Além disso, as instâncias de propriedade que aparecem em qualquer lugar dentro de uma instância de opção são eliminadas durante a validação, a menos que o documento PrintCapabilities contenha uma opção que seja uma correspondência perfeita. Duas instâncias de opção são uma correspondência perfeita se cada ScoredProperty em uma instância de opção tiver um ScoredProperty correspondente no outro e os valores das instâncias de ScoredProperty forem os mesmos. Consulte o esquema privado do provedor PrintTicket para obter uma lista de instâncias de propriedade privada reconhecidas e seus usos.

13. Os filhos do mesmo tipo de elemento não podem aninhar uma profundidade de mais de 10 elementos. Essa regra se aplica de forma independente a cada tipo de elemento que pode ser definido.

> [!Note]  
> O conteúdo XML do PrintTicket deve ser codificado usando UTF-8 ou UTF-16.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



