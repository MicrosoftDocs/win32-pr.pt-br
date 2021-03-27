---
description: Um ícone personalizado deve ser atribuído a um tipo de arquivo para fornecer uma indicação visual ao usuário desse tipo de arquivo ou ao aplicativo ao qual o tipo de arquivo está associado.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Como atribuir um ícone personalizado a um tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967917"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Como atribuir um ícone personalizado a um tipo de arquivo

Quando nenhum ícone padrão personalizado é atribuído a um tipo de arquivo, a área de trabalho e o Windows Explorer exibem todos os arquivos desse tipo com um ícone padrão genérico. Por exemplo, a captura de tela a seguir mostra esse ícone padrão usado com o arquivo MyDocs4. MYP.

![captura de tela do ícone padrão](images/icon.png)

Embora todos os arquivos exibidos nesta captura de tela sejam arquivos de texto simples, somente MyDocs4. MYP exibe o ícone padrão do Windows. Isso ocorre porque a extensão. txt é um tipo de arquivo registrado que tem um ícone padrão personalizado.

A captura de tela a seguir mostra um ícone personalizado que foi atribuído ao tipo de arquivo. MYP.

![captura de tela do ícone personalizado para arquivos. MYP](images/context4.png)

> [!Note]  
> Os ícones também podem ser atribuídos de acordo com uma base específica do aplicativo.

 

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Crie uma subchave chamada **DefaultIcon** em um dos dois locais a seguir:

-   Para uma atribuição de tipo de arquivo, **HKEY \_ classes \_ raiz** \\ *. Extension*
-   Para uma atribuição de aplicativo, **HKEY \_ classes \_ raiz** \\ *ProgID*

### <a name="step-2"></a>Etapa 2:

Atribua a subchave **DefaultIcon** a um valor padrão do tipo **reg \_ sz** que especifica o caminho totalmente qualificado para o arquivo que contém o ícone.

### <a name="step-3"></a>Etapa 3:

Chame a função [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para notificar o Shell para atualizar seu cache de ícone.

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra uma exibição detalhada das entradas do registro que são necessárias para uma atribuição de ícone de tipo de arquivo. A extensão de nome de arquivo é associada a um aplicativo, mas a atribuição de ícone é a própria extensão de nome de arquivo para que o aplicativo associado não dite o ícone padrão.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

O exemplo a seguir mostra uma exibição detalhada das entradas do registro que são necessárias para uma atribuição de ícone de aplicativo. A extensão de nome de arquivo. MYP é associada primeiro ao aplicativo myprogram. 1. A subchave myprogram. 1 ProgID é então atribuída ao ícone padrão personalizado.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Qualquer arquivo que contenha um ícone é aceitável, incluindo arquivos. ico,. exe e. dll. Se houver mais de um ícone no arquivo, o caminho deverá ser seguido por uma vírgula e, em seguida, o índice do ícone.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> </dl>

 

 



