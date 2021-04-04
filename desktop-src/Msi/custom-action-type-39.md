---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 39 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Tipo de ação personalizada 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828875"
---
# <a name="custom-action-type-39"></a>Tipo de ação personalizada 39

O tipo de ação personalizada 39 é usado com instalações simultâneas. As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público. Para obter informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).

Digite 39 ação personalizada instala um aplicativo que é anunciado ou já instalado. Esse tipo de ação personalizada pode ser usado para reinstalar ou remover um produto que foi instalado como uma instalação simultânea pelo pacote de instalação do produto atual. O tipo 39 ação personalizada não pode ser usado para reinstalar ou remover qualquer produto instalado anteriormente por outros meios. Por exemplo, se o produto secundário for instalado usando um tipo 39, tipo 23 ou ação personalizada do tipo 7 durante a instalação do produto principal, uma ação personalizada de tipo 39 poderá ser usada para remover o produto secundário quando o produto primário for desinstalado.

## <a name="source"></a>Fonte

O campo origem da [tabela CustomAction](customaction-table.md) contém o código do produto para o aplicativo.

## <a name="numeric-type"></a>Tipo numérico



| Nome do tipo                                                     | Valor |
|---------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory | 39    |



 

## <a name="target"></a>Destino

O campo de destino da [tabela CustomAction](customaction-table.md) contém configurações de propriedade que devem ser passadas para a instalação simultânea. Essas configurações de propriedade podem especificar recursos.

## <a name="return-processing-options"></a>Opções de processamento de retorno

O tipo de ação personalizada 39 falhará se o aplicativo não for anunciado ou instalado. Para evitar essa falha, você deve definir o **msidbCustomActionTypeContinueflag**.

Uma instalação simultânea não pode ser executada de forma assíncrona.

Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Sinalizadores de opções estão disponíveis para controlar a possível execução de várias ações personalizadas. Consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

A ação personalizada não usa essa opção.

## <a name="return-values"></a>Valores de retorno

O status de retorno da saída do usuário, falha, suspensão ou êxito de uma instalação simultânea é processado da mesma maneira que qualquer outra ação. No entanto, observe que Windows Installer converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log. Por exemplo, se o valor de retorno da ação aparecer como 1 no arquivo de log, isso significa que a ação retornou êxito de erro \_ . Para obter mais informações, consulte [log de valores de retorno de ação](logging-of-action-return-values.md).

Observe que, se uma instalação simultânea tiver **msidbCustomActionTypeContinue** definido, um retorno de erro \_ instalar o \_ usersair, erro de \_ instalação \_ reinicializar, erro de \_ instalação \_ inicial \_ agora ou \_ reinicialização de êxito de erro \_ \_ necessária é tratada como êxito de erro \_ . Isso significa que, se você definir **msidbCustomActionTypeContinue** e sua instalação simultânea exigir uma reinicialização, o requisito para a reinicialização será ignorado. Além disso, o código de erro da ação personalizada de instalação simultânea será ignorado.

Se **msidbCustomActionTypeContinue** não for definido, os códigos de retorno a seguir mais o sucesso do erro \_ serão tratados como sucesso e terão os seguintes significados. Outros códigos de retorno são tratados como falha.



| Mensagem                          | Significado                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| ERRO ao \_ instalar a \_ reinicialização           | O sinalizador de reinicialização será definido para reiniciar no final da instalação.                                  |
| ERRO ao \_ instalar \_ reinicializar \_ agora      | Uma reinicialização é necessária antes de concluir a instalação. A reinicialização será processada imediatamente. |
| ERRO \_ de \_ reinicialização bem-sucedida \_ necessária | Uma reinicialização era necessária, mas foi suprimida.                                                          |



 

## <a name="remarks"></a>Comentários

Uma expressão condicional é necessária para habilitar a instalação simultânea em qualquer instalação ou remoção do componente ou recurso associado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instalações simultâneas](concurrent-installations.md)
</dt> <dt>

[Referência de ação personalizada](custom-action-reference.md)
</dt> <dt>

[Sobre ações personalizadas](about-custom-actions.md)
</dt> <dt>

[Usando ações personalizadas](using-custom-actions.md)
</dt> </dl>

 

 



