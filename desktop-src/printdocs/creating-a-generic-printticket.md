---
description: Saiba como construir um PrintTicket genérico, caso o documento PrintCapabilities para o dispositivo não esteja disponível.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Criando um PrintTicket genérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f660b2f1c015e0d32f5bfd80d58cae96cf3450dfafb13a7758c644ad0a7576b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719726"
---
# <a name="creating-a-generic-printticket"></a>Criando um PrintTicket genérico

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Se o documento PrintCapabilities do dispositivo estiver indisponível ou se o dispositivo de destino for desconhecido, você deverá construir um PrintTicket genérico. Como não há nenhum documento de PrintCapabilities que forneça um conjunto de elementos de recursos e opções, ou parâmetros, as instâncias com suporte desses tipos de elementos devem ser obtidas diretamente das palavras-chave do esquema de impressão.

As etapas mostradas na lista a seguir devem ser usadas quando você cria um PrintTicket genérico.

1.  Crie um documento XML vazio que contenha a raiz do PrintTicket. Atribua um prefixo de namespace ao namespace de esquema de impressão. Especifique a versão do esquema.

2.  Examine as instâncias de recurso nas palavras-chave do esquema de impressão e determine quais delas você deseja definir em seu PrintTicket. Adicione essas instâncias de recursos ao seu PrintTicket. Ao transferir um subrecurso, você deve transferir o recurso pai e preservar a relação pai-filho entre o recurso e o subrecurso no PrintTicket.

    Para cada instância de recurso que você transferir, determine quais instâncias de opção são aplicáveis ao seu PrintTicket. A partir desse conjunto de instâncias de opção, transfira cada instância de opção inteira como ela aparece no esquema de impressão e, em seguida, remova todas as instâncias de propriedade que estão presentes, com a possível exceção daqueles que têm significado em seu PrintTicket. Mantenha todas as instâncias de ScoredProperty, garantindo que você preserve sua localização; Eles são parte intrínseca da definição de opção.

3.  Você também pode adicionar instâncias de propriedade a qualquer ScoredProperty. Os elementos de propriedade são aplicáveis somente se o provedor PrintTicket suportar explicitamente seu uso. Cada provedor deve documentar a finalidade e o uso de todas as instâncias de propriedade com suporte. Como você não tem idéia de qual provedor processará o PrintTicket, talvez queira acrescentar apenas as instâncias de propriedade com suporte explícito pelo provedor PrintTicket do sistema.

4.  Se as palavras-chave do esquema de impressão definirem a Propriedade SelectionType como PickMany para um recurso específico, você poderá selecionar mais de uma opção para esse recurso, desde que a opção designada como IdentityOption não seja aquela selecionada. IdentityOption no esquema de impressão tem o mesmo efeito que a opção None em arquivos PPD PostScript e arquivos GPD do unidrv; Ele serve como um estado não operacional.

5.  Examine as palavras-chave do esquema de impressão para instâncias ParameterDef que devem ser inicializadas em seu PrintTicket. Para cada instância de ParameterDef, selecione o valor a ser usado na instância de ParameterInit no PrintTicket. Esse valor deve ser do tipo de dados correto, deve estar dentro do intervalo definido na instância ParameterDef e deve atender a todos os outros requisitos especificados na instância ParameterDef. Use uma instância de ParameterInit para inicializar o parâmetro para o valor que você selecionou.

    Se você estiver desenvolvendo um componente de interface do usuário (IU), crie seus métodos de geração de PrintTicket para que os usuários possam inserir o valor para o elemento ParameterInit. Além disso, o método de entrada da interface do usuário deve observar e obedecer a quaisquer restrições de entrada especificadas pelo elemento ParameterDef associado.

6.  Examine o conteúdo de cada instância de opção que aparece no PrintTicket para ocorrências de ParameterRef. Se uma instância ParameterInit correspondente ainda não aparecer no PrintTicket, siga a etapa anterior para criar uma instância ParameterInit no PrintTicket. A finalidade dessa instância de ParameterInit é inicializar o parâmetro referenciado pela instância ParameterRef.

7.  Tenha em mente que o dispositivo que processa o trabalho pode não dar suporte a todos os recursos especificados no PrintTicket. Tenha em mente também que um recurso nomeado pode ter suporte, mas uma opção especificada desse recurso pode não ser. As mesmas restrições se aplicam aos parâmetros. Mesmo que um dispositivo dê suporte a um parâmetro nomeado, o valor especificado na instância ParameterInit pode não estar dentro do intervalo válido para o dispositivo.

8.  Examine as palavras-chave do esquema de impressão para as instâncias de propriedade que devem estar presentes em seu PrintTicket. Adicione uma instância de propriedade para cada uma delas ao seu PrintTicket e forneça um valor adequado para ela usando o tipo de elemento de valor. Verifique se as instâncias de propriedade estão localizadas corretamente dentro do PrintTicket. Certifique-se de consultar o esquema PrintTicket em vez do esquema PrintCapabilities.

9.  Examine as instâncias de propriedade opcionais definidas no esquema PrintTicket. Se houver essas instâncias de propriedade que devem estar em seu PrintTicket, crie-as em seu PrintTicket.

10. Os filhos do mesmo tipo de elemento não podem aninhar uma profundidade de mais de 10 elementos. Essa regra se aplica de forma independente a cada tipo de elemento que pode ser definido.

> [!Note]  
> O conteúdo XML do PrintTicket deve ser codificado usando UTF-8 ou UTF-16.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



