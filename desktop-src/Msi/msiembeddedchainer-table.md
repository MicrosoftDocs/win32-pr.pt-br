---
description: Use esta tabela para fazer uma instalação de vários pacotes.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Tabela MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfcf48f3cf3863f19819b3337a136d2540fa3254067cacc50fcf391256caa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945051"
---
# <a name="msiembeddedchainer-table"></a>Tabela MsiEmbeddedChainer

Use esta tabela para autor de uma [instalação de vários pacotes](multiple-package-installations.md). Cada linha na tabela MsiEmbeddedChainer faz referência a uma função diferente definida pelo usuário que pode ser usada para instalar vários pacotes do instalador Windows de um único pacote. Os [arquivos executáveis](executable-files.md) para as funções definidas pelo usuário são armazenados dentro do pacote Windows Instalador.

**[Windows Instalador 4.0 ou anterior:](not-supported-in-windows-installer-4-0.md)** Sem suporte. Esta tabela está disponível a partir do Windows Installer 4.5.

**Windows Server 2008 R2 com a [função Serviços de Área de Trabalho Remota](../termserv/terminal-services-portal.md) habilitada:** Sem suporte. Uma instalação de vários pacotes usando a tabela MsiEmbeddedChainer falhará se Serviços de Área de Trabalho Remota [função](../termserv/terminal-services-portal.md) estiver habilitada.

Para instalar vários pacotes de um único pacote, uma das funções definidas pelo usuário listadas na tabela MsiEmbeddedChainer deve ter uma instrução condicional no campo Condição que é avaliada para executar a ação. Se mais de uma função tiver uma condição que seja avaliada para ser executado, apenas uma função poderá ser executado. Esse caso é um erro e não é possível garantir qual função será executado. Se outras ações personalizadas são necessárias para a instalação, elas devem ser feitas na tabela [CustomAction e](customaction-table.md) nas tabelas de sequência.

As funções devem ingressar na instalação atual chamando a [**função MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) e devem chamar a [**função MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) para fazer commit da instalação de vários pacotes. Se as funções retornarem antes de **chamar MsiEndTransaction,** o instalador retornará todas as instalações.

A tabela MsiEmbeddedChainer tem as colunas a seguir.



| Coluna             | Tipo                             | Chave | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identificador](identifier.md)     | Y   | N        |
| Condição          | [Condição](condition.md)       | N   | Y        |
| CommandLine        | [Formatado](formatted.md)       | N   | Y        |
| Fonte             | [Customsource](customsource.md) | N   | N        |
| Tipo               | [Inteiro](integer.md)           | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

A chave primária da tabela. Esse valor é um identificador exclusivo para a função definida pelo usuário descrita por esta linha.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condição
</dt> <dd>

Uma instrução condicional para executar a função definida pelo usuário. Você pode habilitar ou desabilitar as funções listadas na tabela MsiEmbeddedChainer usando uma transformação que modifica os valores de propriedade avaliados por esse campo. Para obter mais informações, [consulte Usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md).

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>Commandline
</dt> <dd>

O valor nesse campo é uma parte da cadeia de caracteres de linha de comando passada para o arquivo executável identificado na coluna Origem. O instalador anexa o valor nesse campo ao handle de transação para gerar a linha de comando. Se o valor nessa coluna for nulo, a linha de comando consisti somente no alça de transação.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fonte
</dt> <dd>

O local do arquivo executável para a função definida pelo usuário. Se o valor na coluna Tipo for 2, essa coluna poderá conter uma chave externa na [tabela Binária](binary-table.md). Se o valor na coluna Tipo for 18, essa coluna poderá conter uma chave externa na [tabela Arquivo](file-table.md). Se o valor na coluna Tipo for 50, essa coluna poderá conter uma chave externa na [tabela Propriedade](property-table.md).

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

As funções listadas na tabela MsiEmbeddedChainer são descritas usando os seguintes tipos numéricos de ação personalizada. Essa coluna pode conter os valores apenas para os três tipos numéricos a seguir; qualquer outra combinação de sinalizadores de ação personalizada é ignorada.



| Tipo de ação personalizado                                 | Sinalizadores de ação personalizados                                                | Hexadecimal | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Tipo de ação personalizada 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Tipo de ação personalizada 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Tipo de ação personalizada 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O Windows instalador não impede que as funções definidas pelo usuário nesta tabela seja executado durante o anúncio do aplicativo. Você pode usar uma instrução condicional na coluna Condição para impedir que uma função seja executado durante o anúncio.

O Windows instalador também fornece um manipulador de interface do usuário externo não inserido para criar uma interface do usuário rica sobre o pacote Windows Instalador. Para obter mais informações sobre como usar um manipulador de interface do usuário externo com o instalador Windows, consulte [Monitoring an Installation Using MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).

A [Tabela MsiPackageCertificate](msipackagecertificate-table.md) lista certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem uma instalação de vários pacotes. Você pode usar essa tabela para reduzir o número de vezes que [*sua*](u-gly.md) instalação de vários pacotes exibe um prompt de UAC (Controle de Conta de Usuário) que requer uma resposta de um administrador.

 

 
