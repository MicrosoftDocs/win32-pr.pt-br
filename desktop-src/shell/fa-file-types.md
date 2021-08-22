---
description: Este tópico explica como criar novos tipos de arquivo e como associar seu aplicativo ao tipo de arquivo e a outros tipos de arquivo bem definidos.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 541e6068237b504ea8c9faf06e2083986ed5bb48a7c16dabb82e5096569d9f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094201"
---
# <a name="file-types"></a>Tipos de arquivo

Este tópico explica como criar novos tipos de arquivo e como associar seu aplicativo ao tipo de arquivo e a outros tipos de arquivo bem definidos. Arquivos com uma extensão de nome de arquivo comum compartilhada (.doc, .html e assim por diante) são do mesmo *tipo*. Por exemplo, se você criar um novo editor de texto, poderá usar o tipo de arquivo .txt existente. Em outros casos, talvez seja necessário criar um novo tipo de arquivo.

Este tópico é organizado da seguinte forma:

-   [Tipos de arquivo público e privado](#public-and-private-file-types)
-   [Registrando um tipo de arquivo](#registering-a-file-type)
    -   [Definindo subkeys opcionais e atributos de extensão de tipo de arquivo](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Excluindo informações do Registro durante a desinstalação](#deleting-registry-information-during-uninstallation)
-   [Tipos de arquivo que suportam metadados abertos](#file-types-that-support-open-metadata)
-   [Tópicos relacionados](#related-topics)

Informações adicionais podem ser encontradas nos seguintes tópicos:

-   [Como escolher uma extensão de tipo de arquivo](how-to-choose-a-file-type-extension.md)
-   [Como definir atributos de tipo de arquivo](./how-to-define-file-type-attributes.md)
-   [Como incluir um aplicativo na caixa de Abrir com caixa de diálogo](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Como excluir um aplicativo da caixa de diálogo Abrir com para tipos de arquivo nãossociados](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Tipos de arquivo público e privado

Os tipos de arquivo público também são conhecidos como tipos populares ou contenciosos porque os aplicativos concorrentes podem querer ser associados a esses tipos de arquivo. As características dos tipos de arquivo público incluem:

-   Normalmente, eles são definidos por corpos de padrões e/ou são promovidos por suas organizações de definição como formatos de intercâmbio.
-   Geralmente, eles são trocados entre computadores e usuários para finalidades diversas.
-   Eles precisam ter suporte em várias plataformas diferentes.
-   É provável que aplicativos de vários fornecedores os manipularão.

Alguns exemplos de tipos de arquivo que são considerados públicos são os tipos de arquivo de imagem .png, .gif, .jpg e .bmp e os tipos de áudio .wav, .mp3 e .au.

Ao contrário dos tipos de arquivo público, tipos de arquivo particulares ou proprietários normalmente têm um formato implementado e compreendido por apenas um aplicativo ou fornecedor. Como resultado, os tipos de arquivo privado normalmente não são propensos a conflitos entre aplicativos. Alguns tipos de arquivo podem começar como tipos de arquivo privados, mas posteriormente se tornam tipos de arquivo públicos.

> [!Note]  
> Windows diferencia os tipos de arquivo público e privado. A distinção é relevante apenas na tomada de decisões sobre sua escolha de registro de tipo de arquivo.

 

## <a name="registering-a-file-type"></a>Registrando um tipo de arquivo

Para associar o tipo de arquivo a um aplicativo existente, localize o ProgID do aplicativo no Registro. Para associar o tipo de arquivo a um novo aplicativo, defina um ProgID para seu aplicativo. Para obter informações sobre como definir um novo ProgID, consulte [Identificadores programáticos.](fa-progids.md)

As sub-chaves de extensão de nome de arquivo têm o seguinte formato geral: *extensão* = *ProgID.* As sub-chaves de extensão de nome de arquivo são armazenadas na **subárvore \_ RAIZ de \_ CLASSES HKEY.**

É importante incluir o período à frente (.) ao criar subkeys de tipo de arquivo no Registro. Por exemplo, se você quiser que um tipo de arquivo com a extensão curta .myp e a extensão longa .myp-file seja aberto com um aplicativo chamado MyProgram, use a seguinte sintaxe:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Conforme demonstrado no exemplo anterior, se você também registrar uma extensão de nome de arquivo curto (.myp), deverá criar uma sub-chave para a extensão longa (.myp-file) também. Para obter mais informações, consulte [Manipuladores de tipo de arquivo](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Definindo subkeys opcionais e atributos de extensão de tipo de arquivo

As entradas de extensão de tipo de arquivo no Registro têm várias sub-chaves e atributos opcionais.

As entradas de extensão de tipo de arquivo usadas por associações de arquivo são descritas na tabela a seguir. Todos os valores são do **tipo REG \_ SZ.**



| Entrada de registro  | Ação                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Padrão         | De definir o valor padrão da sub-chave de extensão para o ProgID ao qual ela está vinculada.                                                                                                                                                                                                                                                 |
| Tipo de conteúdo    | De definir o valor do Tipo de Conteúdo como o tipo de conteúdo MIME do tipo de arquivo.                                                                                                                                                                                                                                                                   |
| OpenWithList    | Não use. Essa sub-chave contém uma ou mais sub-chaves de aplicativo para aplicativos que aparecem na entrada da caixa de diálogo Abrir com para o tipo de arquivo e destina-se somente .exe aplicativos em sistemas operacionais antes do **Windows** XP. Em vez disso, use OpenWithProgIds.                                                            |
| OpenWithProgIds | Essa sub-chave contém uma lista de ProgIDs alternativos para esse tipo de arquivo. Os programas para esses ProgIDs aparecem no menu **Abrir com** e estão disponíveis como padrão Windows Store para o tipo de arquivo. Sempre que um aplicativo assumir esse tipo de arquivo alterando o valor padrão, ele também deverá adicionar uma entrada a essa lista. |
| PerceivedType   | De definir o valor PerceivedType como o PerceivedType ao qual o arquivo pertence, se for o caso. Essa cadeia de caracteres não é usada Windows versões anteriores ao Windows Vista. Para obter mais informações, consulte [Tipos percebidos e Registro de aplicativo.](fa-perceivedtypes.md)                                                                           |



 

A forma geral de uma sub-chave de extensão de nome de arquivo é a seguinte. Todos os tipos de entrada são do **tipo REG \_ SZ.**

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

-   A **subárvore \_ \_ RAIZ** DE CLASSES HKEY é uma exibição formada pela mesclação de classes de software do usuário atual **HKEY \_ \_** e classes \\  \\  de software **HKEY \_ LOCAL \_ MACHINE** \\  \\ 
-   Em geral, **o HKEY \_ CLASSES \_ ROOT** destina-se a ser lido, mas não gravado. Para obter mais informações, consulte o [artigo RAIZ de CLASSES \_ \_ HKEY.](../sysinfo/hkey-classes-root-key.md)
-   Para registrar um tipo de arquivo globalmente em um computador específico, crie uma entrada para o tipo de arquivo na sub-chave **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Classes.**
-   Para tornar um registro de tipo de arquivo visível somente para o usuário atual, crie uma entrada para o tipo de arquivo na sub-chave classes de software **HKEY \_ CURRENT \_ USER.** \\  \\ 
-   Um aplicativo pode fornecer sua própria implementação de um verbo, como abrir ou reproduzir, conforme mostrado no exemplo de registro a seguir.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Subkeys da sub-chave do verbo incluem a linha de comando e o método de destino drop: **command** e **DropTarget**.

-   Quando você cria ou altera uma associação de arquivo, é importante notificar o sistema de que você fez uma alteração. Faça isso chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) e especificando o **evento \_ SHCNE ASSOCCHANGED.** Se você não chamar **SHChangeNotify**, a alteração poderá não ser reconhecida até que o sistema seja reinicializado.
-   Para recuperar informações do Registro sobre uma associação de arquivo, use a interface [**IQueryAssociations.**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) Para um cenário que ilustra esse procedimento, consulte Cenário de exemplo [de associação de arquivo](fa-sample-scenarios.md).

> [!Note]  
> As  sub-chaves  do Registro de Aplicativos e Caminhos de Aplicativos são usadas para registrar e controlar o comportamento do sistema em nome de aplicativos. Para obter informações mais detalhadas sobre essa funcionalidade, consulte [Registro de aplicativo.](app-registration.md)

 

### <a name="deleting-registry-information-during-uninstallation"></a>Excluindo informações do Registro durante a desinstalação

Ao desinstalar um aplicativo, os ProgIDs e a maioria das outras informações do Registro associadas a esse aplicativo devem ser excluídos como parte da desinstalação. No entanto, os aplicativos que se apropriam de um tipo de arquivo (definindo o valor Padrão da sub-chave .extension ROOT .extension de **\_ \_ CLASSES HKEY** do tipo de arquivo como ProgID do aplicativo) não devem tentar remover esse valor durante a \\  desinstalação. Deixar os dados em prática para o valor Padrão evita a dificuldade de determinar se outro aplicativo se a propriedade do tipo de arquivo foi tomada e substituído pelo valor Padrão depois que o aplicativo original foi instalado. Windows respeitará o valor Padrão somente se o ProgID tiver encontrado um ProgID registrado. Se o ProgID não tiver registro, ele será ignorado.

Observe que outras informações de propriedade de tipo de arquivo são armazenadas na subárvore **HKEY \_ CURRENT \_ USER** e também são usadas somente quando o aplicativo referenciado é registrado. Portanto, esses dados não precisam ser removidos ao desinstalar um aplicativo.

Por exemplo, o seguinte mostra o estado do Registro antes de um aplicativo ser desinstalado:

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

O exemplo a seguir mostra o estado dessas mesmas entradas do Registro depois que o aplicativo é desinstalado.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Tipos de arquivo que suportam metadados abertos

No Windows 7 e posteriores, os seguintes tipos de arquivo são suportados por metadados abertos.



| Tipo de arquivo                                                               | Extensões de nome de arquivo                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Office documentos 2007                                                   | .docx, .xlsx, .pptx                                           |
| Office documentos 97-2003                                                | .doc, .xls, .ppt                                              |
| Pesquisa Salva                                                            | .search-ms                                                    |
| Windows Formatos baseados em mídia (contêiner ASF (Advanced Streaming Format) | .wmv, .wma                                                    |
| MP4 (manipulador de propriedades)                                                  | .mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro de aplicativo](app-registration.md)
</dt> <dt>

[Como funcionam as associações de arquivos](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de Tipo de Arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos percebidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 
