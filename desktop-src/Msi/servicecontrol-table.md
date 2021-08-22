---
description: A tabela de controle de serviço é usada para controlar os serviços instalados ou desinstalados. Observação os serviços que dependem da presença de um assembly no GAC (cache de assembly global) não podem ser instalados ou iniciados usando as tabelas do serviço de instalação e de controle.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabela de UserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b8531fb70c1887d77ae9b09bf3fe7e59de0c7878dfac44707df942e838f4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039976"
---
# <a name="servicecontrol-table"></a>Tabela de UserControl

A tabela de controle de serviço é usada para controlar os serviços instalados ou desinstalados.

> [!Note]  
> Os serviços que dependem da presença de um [assembly](assemblies.md) no GAC (cache de assembly global) não podem ser instalados ou iniciados usando as tabelas de serviço e serviço de [instalação](serviceinstall-table.md) . Se você precisar iniciar um serviço que depende de um assembly no GAC, deverá usar uma ação personalizada sequenciada após a [ação InstallFinalize](installfinalize-action.md) ou uma [ação personalizada Commit](commit-custom-actions.md). Para obter informações sobre como instalar assemblies no GAC, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md).

 

A tabela de controle de origem tem as colunas a seguir.



| Coluna         | Tipo                         | Chave | Nullable |
|----------------|------------------------------|-----|----------|
| ServiceControl | [Identificador](identifier.md) | Y   | N        |
| Nome           | [Binário](formatted.md)   | N   | N        |
| Evento          | [Inteiro](integer.md)       | N   | N        |
| Argumentos      | [Binário](formatted.md)   | N   | Y        |
| Aguarde           | [Inteiro](integer.md)       | N   | Y        |
| Componente\_    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

Esta é a chave primária desta tabela.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Esta coluna é a cadeia de caracteres que nomeia o serviço. Esta coluna pode ser usada para controlar um serviço que não está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância
</dt> <dd>

Esta coluna contém as operações a serem executadas no serviço nomeado. Observe que, ao parar um serviço, todos os serviços que dependem desse serviço também são interrompidos. Ao excluir um serviço que está em execução, o instalador interrompe o serviço.

Os valores nesse campo são campos de bits que podem ser combinados em um único valor que representa várias operações.

Os valores a seguir são usados apenas durante uma instalação.



| Constante                           | Hexadecimal | Decimal | Descrição                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | Inicia o serviço durante a [ação iniciarservices](startservices-action.md).    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | Interrompe o serviço durante a [ação StopServices](stopservices-action.md).       |
| (nenhum)                             | 0x004       | 4       | <reserved>                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | Exclui o serviço durante a [ação DeleteServices](deleteservices-action.md). |



 

Os valores a seguir são usados apenas durante uma desinstalação.



| Constante                                    | Hexadecimal | Decimal | Descrição                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | Inicia o serviço durante a [ação iniciarservices](startservices-action.md).    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | Interrompe o serviço durante a [ação StopServices](stopservices-action.md).       |
| (nenhum)                                      | 0x040       | 64      | <reserved>                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | Exclui o serviço durante a [ação DeleteServices](deleteservices-action.md). |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos
</dt> <dd>

Uma lista de argumentos para iniciar serviços. Os argumentos são separados por caracteres nulos \[ ~ \] . Por exemplo, a lista de argumentos um, dois e três são listados como: um \[ ~ \] dois \[ ~ \] três.

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Esperado
</dt> <dd>

Deixar esse campo nulo ou inserir um valor de 1 faz com que o instalador Aguarde um máximo de 30 segundos para que o serviço seja concluído antes de continuar. A espera pode ser usada para permitir um tempo adicional para um evento crítico retornar um erro de falha. Um valor de 0 neste campo significa aguardar somente até que o SCM (Gerenciador de controle de serviço) informe que esse serviço está em um estado pendente antes de continuar com a instalação.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa para a coluna um da [tabela de componentes](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [startservices](startservices-action.md), [StopServices](stopservices-action.md)e [DeleteServices](deleteservices-action.md) em [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

Use a coluna Nome para iniciar, parar ou excluir serviços que estão sendo substituídos pela instalação ou que dependem de um novo serviço que está sendo instalado. Por exemplo, inserir MyService na coluna ServiceControl pode ligar esse serviço a MyComponent na coluna \_ Componente. Se o campo bit na coluna Evento estiver definido para iniciar durante a instalação, o instalador iniciará MyService ao instalar o MyComponent.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



