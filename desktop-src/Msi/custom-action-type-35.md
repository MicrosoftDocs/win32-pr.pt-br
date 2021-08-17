---
description: os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 35 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo de ação personalizada 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a724fa5a7fc469ea688c64e5935242f088c010da02d963f2f1dc4b05f5eb5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947964"
---
# <a name="custom-action-type-35"></a>Tipo de ação personalizada 35

Essa ação personalizada define o diretório de instalação de uma cadeia de caracteres de texto formatada. Para obter mais informações, consulte [alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)

## <a name="source"></a>Fonte

O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de diretórios](directory-table.md). O diretório designado é definido pela cadeia de caracteres formatada no campo de destino usando [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha). Isso define o caminho de destino e a propriedade associada para o valor expandido da cadeia de caracteres de texto formatado no campo de destino. Não tente alterar o local de um diretório de destino durante uma [instalação de manutenção](maintenance-installation.md). Não tente alterar o caminho do diretório de destino se alguns componentes que usam esse caminho já estiverem instalados para qualquer usuário.

## <a name="type-value"></a>Valor do tipo

Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.



| Constantes                                                              | Hexadecimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>Destino

A coluna Target da [tabela CustomAction](customaction-table.md) contém uma cadeia de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico). Os parâmetros a serem substituídos são colocados entre colchetes \[ ... \] e podem ser Propriedades, variáveis de ambiente (% Prefix), caminhos de arquivo ( \# prefixo) ou caminhos de diretório de componente ($ Prefix). Observe que os caminhos de diretório sempre terminam com um separador de diretório.

## <a name="return-processing-options"></a>Opções de processamento de retorno

A ação personalizada não usa essas opções.

## <a name="execution-scheduling-options"></a>Opções de agendamento de execução

Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução. Essas opções controlam a execução de várias ações personalizadas. Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opções de execução de In-Script

A ação personalizada não usa essas opções.

## <a name="return-values"></a>Valores de retorno

Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).

## <a name="remarks"></a>Comentários

Se você definir uma [propriedade privada](private-properties.md) na sequência da interface do usuário criando uma ação personalizada em uma das tabelas de sequência da interface do usuário, essa propriedade não será definida na sequência de execução. Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução. Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na [**Propriedade SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Ações personalizadas](custom-actions.md)
</dt> <dt>

[Ações personalizadas de texto formatado](formatted-text-custom-actions.md)
</dt> </dl>

 

 



