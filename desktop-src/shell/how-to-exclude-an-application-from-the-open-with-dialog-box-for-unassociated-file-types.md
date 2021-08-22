---
description: Como excluir um aplicativo da caixa de diálogo abrir com para o tipo de arquivo não associado.
title: Como excluir um aplicativo da caixa de diálogo abrir com para tipos de arquivo não associados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d90ae5ab49128df1eedd9b760286ce54f6b6498cbe00d4a945145a80f956cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350906"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Como excluir um aplicativo da caixa de diálogo abrir com para tipos de arquivo não associados

Quando um usuário tenta abrir um arquivo que não é membro de nenhum tipo de arquivo registrado (ou seja, um tipo de arquivo desconhecido) ou quando um usuário seleciona **abrir com** ou **abrir com-> escolher programa padrão** no menu de atalho de um arquivo, o Shell apresenta um submenu ou caixa de diálogo que permite ao usuário especificar o programa usado para abrir o arquivo.

Por padrão, qualquer aplicativo registrado como uma subchave de aplicativos **\_ \_ raiz de classes hKey** \\  é apresentado na caixa de diálogo **abrir com** . Esses aplicativos são apresentados em **abrir com** , independentemente de o aplicativo estar registrado para lidar com o tipo de arquivo.

Para impedir que um aplicativo apareça na caixa de diálogo **abrir com** quando o aplicativo não deve ou não pode ser usado para abrir determinados tipos de arquivo, use uma das duas técnicas descritas neste tópico.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Adicione uma entrada NoOpenWith à subchave do aplicativo. quando um aplicativo usa um tipo de arquivo, o Windows registra essas informações para criar a lista de **programas recomendados** . Essa lista é apresentada no submenu **abrir com** , conforme mostrado na captura de tela a seguir.

![captura de tela do menu de atalho com o submenu abrir com mostrado](images/file-assoc/openwithsubmenu.png)

Esses aplicativos recomendados também são mostrados na parte **programas recomendados** da caixa de diálogo **abrir com** , conforme mostrado na captura de tela a seguir.

![captura de tela da caixa de diálogo abrir com com programas recomendados](images/file-assoc/openwithdialog.png)

> [!Note]  
> Se um aplicativo se registrou em [OpenWithList](fa-file-types.md) ou OpenWithProgIDs para o tipo de arquivo, ele será exibido na lista de **programas recomendados** , mesmo que a entrada NoOpenWith esteja definida. Além disso, lembre-se de que, independentemente de um aplicativo ser oferecido em uma lista de programas recomendados, um usuário pode navegar manualmente para qualquer arquivo executável.

 

Os aplicativos podem desabilitar esse controle especificando um valor de NoOpenWith sob a subchave do aplicativo.

A entrada NoOpenWith é um valor **\_ sz do reg** vazio, conforme mostrado no exemplo a seguir.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

A definição da entrada NoOpenWith também tem estes efeitos:

-   Impede a fixação de um arquivo na lista de atalhos do aplicativo por meio de arrastar e soltar, a menos que o aplicativo esteja especificamente registrado para lidar com esse tipo de arquivo.
-   Impede que a caixa de diálogo arquivo comum e qualquer chamada para a função [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) adicione qualquer arquivo à lista de atalhos do aplicativo, a menos que o aplicativo esteja especificamente registrado para lidar com esse tipo de arquivo.

### <a name="step-2"></a>Etapa 2:

A segunda maneira de impedir que um aplicativo apareça na caixa de diálogo **abrir com** é usar a subchave **SupportedTypes** para listar explicitamente as extensões dos tipos de arquivos que o aplicativo pode abrir. Isso impede que o aplicativo apareça na caixa de diálogo **abrir com** para os tipos de arquivo que não podem ser abertos. Ele também faz com que o aplicativo apareça na lista de **programas recomendados** , conforme discutido anteriormente.

Esse método é particularmente útil se um aplicativo pode salvar um arquivo como um determinado tipo de arquivo, mas não pode abrir esse tipo de arquivo. Um aplicativo também deve definir o \_ sinalizador FOS DONTADDTORECENT por meio de [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) ao chamar a caixa de diálogo **salvar** . Isso impede que o item seja adicionado às partes **recentes** ou **frequentes** de uma lista de atalhos. Ele também impede que o aplicativo seja acompanhado em [OpenWithList](fa-file-types.md).

Cada extensão com suporte é adicionada como uma entrada na subchave **SupportedTypes** , conforme mostrado no exemplo a seguir. As entradas são do tipo **reg \_ sz** ou **reg \_ NULL**, sem valores associados.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Se uma subchave **SupportedTypes** for fornecida, somente os arquivos com essas extensões estarão qualificados para fixação na lista de atalhos do aplicativo ou para serem rastreados na lista de destinos **recentes** ou **frequentes** de um aplicativo.

A entrada NoOpenWith substitui a subchave **SupportedTypes** e oculta o aplicativo na caixa de diálogo **abrir com** .

 

 
