---
description: Saiba como construir um PrintTicket genérico, caso o documento PrintCapabilities para o dispositivo não está disponível.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Criando um PrintTicket genérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e611205663138b9cc3c0d3cd315c2c19d2d7e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409519"
---
# <a name="creating-a-generic-printticket"></a>Criando um PrintTicket genérico

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Se o documento PrintCapabilities para o dispositivo não estiver disponível ou se o dispositivo de destino for desconhecido, você deverá construir um PrintTicket genérico. Como não há nenhum documento PrintCapabilities que fornece um conjunto de elementos Feature e Option ou parâmetros, as instâncias com suporte desses tipos de elemento devem ser obtidas diretamente das Palavras-chave de esquema de impressão.

As etapas mostradas na lista a seguir devem ser usadas quando você cria um PrintTicket genérico.

1.  Crie um documento XML vazio que contém a raiz PrintTicket. Atribua um prefixo de namespace ao namespace Esquema de Impressão. Especifique a versão do esquema.

2.  Examine as instâncias de recurso nas Palavras-chave de esquema de impressão e determine quais delas você deseja definir em seu PrintTicket. Adicione essas instâncias de recurso ao PrintTicket. Ao transferir uma subfeature, você deve transferir o Recurso pai e preservar a relação pai-filho entre o Recurso e a subfeature no PrintTicket.

    Para cada Instância de recurso que você transferir, determine quais instâncias de Opção são aplicáveis ao PrintTicket. Nesse conjunto de instâncias de Opção, transfira cada instância option inteira como ela aparece no Esquema de Impressão e remova todas as instâncias de Propriedade que estão presentes, com a possível exceção daquelas que têm significância para o PrintTicket. Mantenha todas as instâncias ScoredProperty, certifique-se de preservar sua localização; eles são uma parte intrínseca da definição de Opção.

3.  Você também pode adicionar Instâncias de propriedade a qualquer ScoredProperty. Os elementos de propriedade serão aplicáveis somente se o provedor PrintTicket for explicitamente compatível com seu uso. Cada provedor deve documentar a finalidade e o uso de todas as instâncias de Propriedade com suporte. Como você não tem ideia de qual provedor processará o PrintTicket, talvez você queira anexar apenas as instâncias de Propriedade que têm suporte explícito pelo provedor PrintTicket do sistema.

4.  Se as Palavras-chave de esquema de impressão definirem a propriedade SelectionType como PickMany para um recurso específico, você poderá selecionar mais de uma Opção para esse Recurso, desde que a Opção designada como IdentityOption não seja uma das selecionadas. IdentityOption no Esquema de Impressão tem o mesmo efeito que a opção None em arquivos POSTSCRIPT PPD e arquivos GPD Unidrv; ele serve como uma não operação.

5.  Examine as Palavras-chave de esquema de impressão para instâncias ParameterDef que devem ser inicializadas em seu PrintTicket. Para cada instância parameterDef, selecione o Valor a ser usado na instância ParameterInit no PrintTicket. Esse Valor deve ser do tipo de dados correto, deve estar dentro do intervalo definido na instância parameterDef e deve atender a todos os outros requisitos especificados na instância parameterDef. Use uma instância ParameterInit para inicializar o parâmetro para o Valor selecionado.

    Se você estiver desenvolvendo um componente de interface do usuário, projete seus métodos de geração PrintTicket para que os usuários possam inserir o Valor para o elemento ParameterInit. Além disso, o método de entrada da interface do usuário deve observar e estar em conformidade com as restrições de entrada especificadas pelo elemento ParameterDef associado.

6.  Examine o conteúdo de cada instância option que aparece no PrintTicket em busca de ocorrências de ParameterRef. Se uma instância parameterInit correspondente ainda não aparecer no PrintTicket, siga a etapa anterior para criar uma instância ParameterInit no PrintTicket. A finalidade dessa instância ParameterInit é inicializar o parâmetro referenciado pela instância ParameterRef.

7.  Tenha em mente que o dispositivo que processa o trabalho pode não dar suporte a todos os Recursos especificados no PrintTicket. Tenha em mente também que um Recurso nomeado pode ter suporte, mas uma opção especificada desse recurso pode não ser. As mesmas advertências se aplicam aos parâmetros. Mesmo que um dispositivo seja compatível com um parâmetro nomeado, o Valor especificado na instância parameterInit pode não estar dentro do intervalo válido para o dispositivo.

8.  Examine as Palavras-chave de esquema de impressão para instâncias de propriedade que devem estar presentes em seu PrintTicket. Adicione uma Instância de propriedade para cada um deles ao PrintTicket e forneça um valor adequado para ela usando o tipo de elemento Value. Certifique-se de que as instâncias de Propriedade estão localizadas corretamente dentro do PrintTicket. Certifique-se de consultar o esquema PrintTicket em vez do esquema PrintCapabilities.

9.  Examine as instâncias de Propriedade opcionais definidas no esquema PrintTicket. Se houver essas instâncias de Propriedade que devem estar em seu PrintTicket, crie-as em seu PrintTicket.

10. Os filhos do mesmo tipo de elemento podem não aninhar a uma profundidade de mais de 10 elementos. Essa regra se aplica independentemente a cada tipo de elemento que pode ser definido.

> [!Note]  
> O conteúdo XML printTicket DEVE ser codificado usando UTF-8 ou UTF-16.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



