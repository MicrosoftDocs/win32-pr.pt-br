---
description: Saiba mais sobre os conceitos de Windows Installer que começam com a letra D, como a função de banco de dados e o patch Delta.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d76378d636c8ae14acdc9cb882c31840e3f1550f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010929"
---
# <a name="d-windows-installer"></a>D (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**função de banco de dados**
</dt> <dd>

Acessa o banco de dados do instalador. Essas funções são fornecidas principalmente para uso por [*ferramentas de criação de pacote do instalador*](i-gly.md) e não se destinam a serem usadas para chamar os serviços do instalador. Para obter mais informações, consulte [funções de banco de dados](database-functions.md) e a referência de função do [instalador](installer-function-reference.md).

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**identificador de banco de dados**
</dt> <dd>

Necessário para trabalhar com um banco de dados. Para obter mais informações, consulte [obtendo um identificador de banco de dados](obtaining-a-database-handle.md).

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**patch Delta**
</dt> <dd>

Um patch Delta é um patch de Windows Installer compactado por Delta criado usando uma ferramenta, como Patchwiz.dll, que dá suporte à compactação Delta. Os patches que usam a compactação Delta podem reduzir o tamanho de uma atualização fornecendo apenas as diferenças (deltas) entre os arquivos existentes em um computador de destino e os arquivos novos desejados. Os arquivos novos desejados são então sintetizados a partir dos arquivos existentes e dos deltas baixados. Para obter mais informações sobre a tecnologia de compactação Delta, consulte a [interface de programação de aplicativo de compactação Delta](https://msdn.microsoft.com/library/ms811406.aspx).

</dd> </dl>

 

 



