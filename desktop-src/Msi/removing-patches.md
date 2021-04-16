---
description: A partir do Windows Installer&\# 160; versão&\# 160; 3.0, é possível criar e instalar patches que podem ser desinstalados individualmente e em qualquer ordem, sem precisar desinstalar e reinstalar todo o aplicativo e outros patches.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Removendo patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd54db3bde3a356a0c3adb299555248bbc87a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749985"
---
# <a name="removing-patches"></a>Removendo patches

A partir do Windows Installer versão 3,0, é possível criar e instalar patches que podem ser desinstalados individualmente e em qualquer ordem, sem precisar desinstalar e reinstalar todo o aplicativo e outros patches. Windows Installer 3,0 também permite que [pacotes de patch](patch-packages.md) sejam criados com uma [tabela MsiPatchSequence](msipatchsequence-table.md) que contém informações de sequenciamento de patch. Com versões do Windows Installer anteriores à Windows Installer 3,0, o único método para remover patches específicos de um aplicativo é desinstalar todo o aplicativo corrigido e reinstalá-lo sem reaplicar os patches que estão sendo removidos.

Se um patch pode ser desinstalado depende de como o patch foi criado, a versão do Windows Installer usada para instalar o patch e as alterações feitas pelo patch para o aplicativo. Se um patch não for desinstalado, a única maneira de remover o patch será desinstalar todo o aplicativo e reinstalá-lo sem aplicar o patch que está sendo removido.

Você pode desinstalar um ou mais patches usando uma opção de linha de comando, a interface de script ou chamando [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) de outro aplicativo. Consulte [desinstalando patches](uninstalling-patches.md) para obter mais informações sobre como desinstalar patches.

O valor da propriedade [**MSIPATCHREMOVE**](msipatchremove.md) lista os patches a serem desinstalados. Para cada patch na lista, o instalador verifica se o patch é desinstalado. Se o usuário não tiver privilégios para remover o patch, o patch é desconhecido para o produto, a política de patch impede a remoção ou o patch foi marcado como não desinstalado, o instalador retorna um erro que indica uma falha na transação de instalação. Consulte [patches desinstaláveis](uninstallable-patches.md) para obter mais informações sobre o que determina se um patch não é desinstalável.

Depois que o patch é verificado como removível, o instalador remove o patch da sequência de aplicativos do patch. Para obter mais informações sobre como Windows Installer 3,0 determina qual sequência usar ao aplicar patches, consulte [sequenciando patches](sequencing-patches.md). Observe que a remoção de patches da sequência pode fazer com que os patches marcados como obsoletos ou substituídos se tornem ativos.

Todos os patches selecionados para remoção estão listados na propriedade [**MsiPatchRemovalList**](msipatchremovallist.md) . Essa propriedade é uma propriedade privada que é definida pelo instalador e pode ser usada em expressões condicionais ou consultada por [ações personalizadas](custom-actions.md). A propriedade contém a lista de GUIDs de código de patch de patches a serem removidos. Uma ação personalizada pode determinar se o estado da instalação do patch é aplicado, obsoleto ou substituído chamando o [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou a propriedade [**Patchproperty**](patch-patchproperty.md) do [objeto patch](patch-object.md).

Depois que um patch é removido, o estado do aplicativo é o mesmo que se o patch nunca foi instalado. Se possível, o instalador restringe o processo ao subconjunto de recursos afetados pelo patch que está sendo removido. O instalador define automaticamente a propriedade [**REINSTALL**](reinstall.md) para a lista de recursos afetados. Os arquivos que foram adicionados pelo patch são removidos e os arquivos que foram modificados pelo patch são substituídos. Os arquivos e as entradas do registro são restaurados para a versão esperada pelo produto menos o patch. Os recursos e componentes que foram adicionados pelo patch têm o registro cancelado do aplicativo. Observe que o conteúdo adicional adicionado pelo patch pode permanecer no computador do usuário se o conteúdo for usado por outro patch que ainda é aplicável.

Se um arquivo de um componente compartilhado for atualizado por um patch, a alteração afetará todos os aplicativos que compartilham o componente. Quando o patch é removido, novamente, a alteração afeta todos os aplicativos que compartilham o componente. Isso significa que a remoção de um patch por um aplicativo pode restaurar o arquivo do componente compartilhado para uma versão inferior à necessária para outro aplicativo. Isso poderia corrigir o primeiro aplicativo, mas fazer com que o segundo aplicativo pare de funcionar. Nesse caso, o segundo aplicativo pode ser reparado reinstalando o segundo aplicativo usando os métodos descritos na [reinstalação de um recurso ou aplicativo](reinstalling-a-feature-or-application.md). Isso irá restaurar a versão com patch do arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Sequenciamento de patch](sequencing-patches.md)
</dt> <dt>

[Corrigir ações personalizadas de desinstalação de patch](patch-uninstall-custom-actions.md)
</dt> <dt>

[Patches desinstaláveis](uninstallable-patches.md)
</dt> <dt>

[Desinstalando patches](uninstalling-patches.md)
</dt> </dl>

 

 



