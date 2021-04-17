---
description: Use esta tabela para criar uma instalação de vários pacotes.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Tabela MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902a33bce5d3a0aff3d2797fce94e5d272b61271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757117"
---
# <a name="msiembeddedchainer-table"></a>Tabela MsiEmbeddedChainer

Use esta tabela para criar uma [instalação de vários pacotes](multiple-package-installations.md). Cada linha na tabela MsiEmbeddedChainer faz referência a uma função diferente definida pelo usuário que pode ser usada para instalar vários pacotes de Windows Installer de um único pacote. Os [arquivos executáveis](executable-files.md) para as funções definidas pelo usuário são armazenados dentro do pacote de Windows Installer.

**[Windows Installer 4,0 ou anterior](not-supported-in-windows-installer-4-0.md):** Sem suporte. Esta tabela está disponível a partir do Windows Installer 4,5.

**Windows Server 2008 R2 com a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) habilitada:** Sem suporte. Uma instalação de vários pacotes usando a tabela MsiEmbeddedChainer falhará se a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) estiver habilitada.

Para instalar vários pacotes de um único pacote, uma das funções definidas pelo usuário listadas na tabela MsiEmbeddedChainer deve ter uma instrução condicional no campo condição que é avaliada para executar a ação. Se mais de uma função tiver uma condição que seja avaliada para execução, somente uma função poderá ser executada. Esse caso é um erro e não pode ser garantido qual função será executada. Se outras ações personalizadas forem necessárias para a instalação, elas deverão ser criadas na [tabela CustomAction](customaction-table.md) e nas tabelas de sequência.

As funções devem ingressar na instalação atual chamando a função [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) e devem chamar a função [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) para confirmar a instalação de vários pacotes. Se as funções retornarem antes de chamar **MsiEndTransaction**, o instalador reverterá todas as instalações.

A tabela MsiEmbeddedChainer tem as colunas a seguir.



| Coluna             | Tipo                             | Chave | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identificador](identifier.md)     | S   | N        |
| Condição          | [Condição](condition.md)       | N   | S        |
| CommandLine        | [Binário](formatted.md)       | N   | S        |
| Fonte             | [CustomSource](customsource.md) | N   | N        |
| Tipo               | [Inteiro](integer.md)           | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

A chave primária da tabela. Esse valor é um identificador exclusivo para a função definida pelo usuário descrita por essa linha.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Uma instrução condicional para executar a função definida pelo usuário. Você pode habilitar ou desabilitar as funções listadas na tabela MsiEmbeddedChainer usando uma transformação que modifica os valores de propriedade avaliados por esse campo. Para obter mais informações, consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md).

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>CommandLine
</dt> <dd>

O valor nesse campo é uma parte da cadeia de caracteres de linha de comando passada para o arquivo executável identificado na coluna de origem. O instalador acrescenta o valor nesse campo ao identificador de transação para gerar a linha de comando. Se o valor nessa coluna for nulo, a linha de comando consistirá apenas no identificador de transação.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Original
</dt> <dd>

O local do arquivo executável para a função definida pelo usuário. Se o valor na coluna type for 2, essa coluna poderá conter uma chave externa na [tabela Binary](binary-table.md). Se o valor na coluna tipo for 18, essa coluna poderá conter uma chave externa na tabela de [arquivos](file-table.md). Se o valor na coluna type for 50, essa coluna poderá conter uma chave externa na tabela de [Propriedades](property-table.md).

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

As funções listadas na tabela MsiEmbeddedChainer são descritas usando os seguintes tipos numéricos de ação personalizada. Esta coluna pode conter os valores somente para os três tipos numéricos a seguir; qualquer outra combinação de sinalizadores de ação personalizada é ignorada.



| Tipo de ação personalizada                                 | Sinalizadores de ação personalizada                                                | Hexadecimal | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Tipo de ação personalizada 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Tipo de ação personalizada 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Tipo de ação personalizada 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A Windows Installer não impede que as funções definidas pelo usuário nesta tabela sejam executadas durante o anúncio do aplicativo. Você pode usar uma instrução condicional na coluna condição para impedir que uma função seja executada durante o anúncio.

O Windows Installer também fornece um manipulador de interface do usuário externa não incorporado para criar uma rica interface de usuários sobre o pacote Windows Installer. Para obter mais informações sobre como usar um manipulador de interface do usuário externo com o Windows Installer, consulte [monitorando uma instalação usando o MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).

A [tabela MsiPackageCertificate](msipackagecertificate-table.md) lista os certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem uma instalação de vários pacotes. Você pode usar essa tabela para reduzir o número de vezes que a instalação de vários pacotes exibe um prompt de [*controle de conta de usuário*](u-gly.md) (UAC) que requer uma resposta por um administrador.

 

 
