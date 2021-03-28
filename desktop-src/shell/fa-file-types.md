---
description: Este tópico explica como criar novos tipos de arquivo e como associar seu aplicativo ao tipo de arquivo e a outros tipos de arquivo bem definidos.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967948"
---
# <a name="file-types"></a>Tipos de arquivo

Este tópico explica como criar novos tipos de arquivo e como associar seu aplicativo ao tipo de arquivo e a outros tipos de arquivo bem definidos. Arquivos com uma extensão de nome de arquivo comum compartilhada (. doc,. html e assim por diante) são do mesmo *tipo*. Por exemplo, se você criar um novo editor de texto, poderá usar o tipo de arquivo. txt existente. Em outros casos, talvez seja necessário criar um novo tipo de arquivo.

Este tópico é organizado da seguinte maneira:

-   [Tipos de arquivos públicos e privados](#public-and-private-file-types)
-   [Registrando um tipo de arquivo](#registering-a-file-type)
    -   [Definindo subchaves opcionais e atributos de extensão de tipo de arquivo](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Excluindo informações do registro durante a desinstalação](#deleting-registry-information-during-uninstallation)
-   [Tipos de arquivo que dão suporte a metadados abertos](#file-types-that-support-open-metadata)
-   [Tópicos relacionados](#related-topics)

Informações adicionais podem ser encontradas nos seguintes tópicos:

-   [Como escolher uma extensão de tipo de arquivo](how-to-choose-a-file-type-extension.md)
-   [Como definir atributos de tipo de arquivo](./how-to-define-file-type-attributes.md)
-   [Como incluir um aplicativo na caixa de diálogo abrir com](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Como excluir um aplicativo da caixa de diálogo abrir com para tipos de arquivo não associados](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Tipos de arquivos públicos e privados

Os tipos de arquivo públicos também são conhecidos como tipos populares ou contenciosos porque os aplicativos concorrentes podem querer ser associados a esses tipos de arquivo. As características dos tipos de arquivo públicos incluem:

-   Normalmente, eles são definidos por órgãos de padrões e/ou são promovidos por suas organizações de definição como formatos de intercâmbio.
-   Muitas vezes, eles são trocados entre computadores e usuários para fins diferentes.
-   Eles precisam ter suporte em várias plataformas diferentes.
-   É provável que os aplicativos de vários fornecedores os manipulem.

Alguns exemplos de tipos de arquivo que são considerados públicos são os tipos de arquivo de imagem. png,. gif,. jpg e. bmp, e os tipos de áudio. wav,. mp3 e. au.

Ao contrário dos tipos de arquivos públicos, os tipos de arquivos privados ou proprietários normalmente têm um formato que é implementado e compreendido por apenas um aplicativo ou fornecedor. Como resultado, os tipos de arquivo privados normalmente não são propensos a conflitos entre aplicativos. Alguns tipos de arquivo podem ser iniciados como tipos de arquivo privados, mas posteriormente se tornam tipos de arquivo públicos.

> [!Note]  
> O Windows não diferencia os tipos de arquivo público e privado. A distinção é relevante apenas para tomar decisões sobre a escolha do registro de tipo de arquivo.

 

## <a name="registering-a-file-type"></a>Registrando um tipo de arquivo

Para associar o tipo de arquivo a um aplicativo existente, localize a ProgID do aplicativo no registro. Para associar o tipo de arquivo a um novo aplicativo, defina um ProgID para seu aplicativo. Para obter informações sobre como definir um novo ProgID, consulte [identificadores programáticos](fa-progids.md).

As subchaves de extensão de nome de arquivo têm o seguinte formato geral: ProgID de *extensão* = . As subchaves de extensão de nome de arquivo são armazenadas na subárvore **\_ \_ raiz de classes hKey** .

É importante incluir o ponto à esquerda (.) ao criar subchaves de tipo de arquivo no registro. Por exemplo, se você quiser um tipo de arquivo com a extensão curta. MYP e a extensão longa. MYP-arquivo a ser aberto com um aplicativo chamado myprogram, use a seguinte sintaxe:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Conforme demonstrado no exemplo anterior, se você também registrar uma extensão de nome de arquivo curto (. MYP), deverá criar uma subchave para a extensão longa (. MYP-File) também. Para obter mais informações, consulte [manipuladores de tipo de arquivo](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Definindo subchaves opcionais e atributos de extensão de tipo de arquivo

As entradas de extensão de tipo de arquivo no registro têm várias subchaves e atributos opcionais.

As entradas de extensão de tipo de arquivo usadas por associações de arquivo são descritas na tabela a seguir. Todos os valores são do tipo **reg \_ sz** .



| Entrada de registro  | Ação                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Padrão         | Defina o valor padrão da subchave de extensão para o ProgID ao qual ela está vinculada.                                                                                                                                                                                                                                                 |
| Tipo de conteúdo    | Defina o valor do tipo de conteúdo como o tipo de conteúdo MIME do tipo de arquivo.                                                                                                                                                                                                                                                                   |
| OpenWithList    | Não use. Essa subchave contém uma ou mais subchaves de aplicativo para aplicativos que aparecem na entrada da caixa de diálogo **abrir com** para o tipo de arquivo e destina-se apenas a aplicativos. exe em sistemas operacionais anteriores ao Windows XP. Use OpenWithProgIds em vez disso.                                                            |
| OpenWithProgIds | Essa subchave contém uma lista de ProgIDs alternativos para esse tipo de arquivo. Os programas para esses ProgIDs aparecem no menu **abrir com** e estão disponíveis como aplicativos padrão da Windows Store para o tipo de arquivo. Sempre que um aplicativo assumir esse tipo de arquivo alterando o valor padrão, ele também deverá adicionar uma entrada a essa lista. |
| PerceivedType   | Defina o valor percebido como o percebido ao qual o arquivo pertence, se houver. Essa cadeia de caracteres não é usada pelas versões do Windows anteriores ao Windows Vista. Para obter mais informações, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).                                                                           |



 

A forma geral de uma subchave de extensão de nome de arquivo é a seguinte. Todos os tipos de entrada são do tipo **reg \_ sz** .

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

Considerações importantes sobre tipos de arquivo incluem:

-   A subárvore **\_ \_ raiz de classes hKey** é uma exibição formada pela mesclagem do **HKEY \_ Current \_ User** \\ **software** \\ **classes** e o **HKEY \_ local \_ Machine** \\ **software** \\ **classes**
-   Em geral, **a \_ \_ raiz de classes hKey** deve ser lida, mas não gravada. Para obter mais informações, consulte o artigo [ \_ \_ raiz de classes hKey](../sysinfo/hkey-classes-root-key.md) .
-   Para registrar um tipo de arquivo globalmente em um computador específico, crie uma entrada para o tipo de arquivo na subchave **HKEY \_ local \_ Machine** \\ **software** \\ **classes** .
-   Para tornar um registro de tipo de arquivo visível somente para o usuário atual, crie uma entrada para o tipo de arquivo na subchave **HKEY \_ Current \_ User** \\ **software** \\ **classes** .
-   Um aplicativo pode fornecer sua própria implementação de um verbo, como Open ou Play, conforme mostrado no exemplo de registro a seguir.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Subchaves da subchave Verb incluem a linha de comando e o método Drop target: **Command** e **DropTarget**.

-   Quando você cria ou altera uma associação de arquivo, é importante notificar o sistema de que você fez uma alteração. Faça isso chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) e especificando o evento **SHCNE \_ assocchanged** . Se você não chamar **SHChangeNotify**, a alteração poderá não ser reconhecida até que o sistema seja reinicializado.
-   Para recuperar informações de registro sobre uma associação de arquivo, use a interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) . Para ver um cenário que ilustra esse procedimento, consulte [exemplo de associação de arquivo](fa-sample-scenarios.md).

> [!Note]  
> As subchaves de registro de **aplicativos** e **caminhos de aplicativo** são usadas para registrar e controlar o comportamento do sistema em nome dos aplicativos. Para obter informações mais detalhadas sobre essa funcionalidade, consulte [registro de aplicativo](app-registration.md).

 

### <a name="deleting-registry-information-during-uninstallation"></a>Excluindo informações do registro durante a desinstalação

Ao desinstalar um aplicativo, os ProgIDs e a maioria das outras informações de registro associadas a esse aplicativo devem ser excluídos como parte da desinstalação. No entanto, os aplicativos que assumiram a propriedade de um tipo de arquivo (definindo o valor padrão da subchave **HKEY \_ classes \_ raiz**. Extension do tipo de arquivo \\  para o ProgID do aplicativo) não devem tentar remover esse valor ao desinstalar o. Deixar os dados em vigor para o valor padrão evita a dificuldade de determinar se outro aplicativo assumiu a propriedade do tipo de arquivo e substituiu o valor padrão após a instalação do aplicativo original. O Windows respeita o valor padrão somente se o ProgID encontrado há um ProgID registrado. Se o ProgID tiver o registro cancelado, ele será ignorado.

Observe que outras informações de propriedade de tipo de arquivo são armazenadas na subárvore **\_ atual do \_ usuário do hKey** e também são usadas somente quando o aplicativo ao qual ele faz referência é registrado. Portanto, esses dados não precisam ser removidos durante a desinstalação de um aplicativo.

Por exemplo, o seguinte mostra o estado do registro antes de um aplicativo ser desinstalado:

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

O seguinte mostra o estado dessas mesmas entradas de registro depois que o aplicativo é desinstalado.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Tipos de arquivo que dão suporte a metadados abertos

No Windows 7 e posterior, os seguintes tipos de arquivo dão suporte a metadados abertos.



| Tipo de arquivo                                                               | Extensões de nome de arquivo                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Documentos do Office 2007                                                   | . docx,. xlsx,. pptx                                           |
| Documentos do Office 97-2003                                                | . doc,. xls,. ppt                                              |
| Pesquisa Salva                                                            | . Search-MS                                                    |
| Formatos baseados no Windows Media (ASF (Advanced Streaming Format)) | . wmv,. WMA                                                    |
| MP4 (manipulador de propriedade)                                                  | . MP4,. M4A,. m4v,. MP4V,. M4P,. M4B,. 3GP,. 3GPP,. 3GP2,. mov |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[registro de Aplicativo](app-registration.md)
</dt> <dt>

[Como funcionam as associações de arquivo](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de tipo de arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos observados](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 
