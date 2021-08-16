---
description: O Shell usa uma sub-chave do Registro progID (identificador programático) para associar um tipo de arquivo a um aplicativo e controlar o comportamento da associação.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificadores programáticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdc29a3981461a178bdf528768bb12b1840ac5dbed46f310c10718fa9429153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860803"
---
# <a name="programmatic-identifiers"></a>Identificadores programáticos

O Shell usa uma sub-chave do Registro progID (identificador programático) para associar um tipo de arquivo a um aplicativo e controlar o comportamento da associação. As entradas ProgID usadas para associações de arquivo estão localizadas em **HKEY \_ CLASSES \_ ROOT** no Registro.

Este tópico é organizado da seguinte forma:

-   [Elementos de identificador programático usados por associações de arquivo](#programmatic-identifier-elements-used-by-file-associations)
-   [Usando identificadores programáticos com versão](#using-versioned-programmatic-identifiers)
-   [Tópicos relacionados](#related-topics)

Para obter informações adicionais, [leia Como registrar um tipo de arquivo para um novo aplicativo](how-to-register-a-file-type-for-a-new-application.md)

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Elementos de identificador programático usados por associações de arquivo

O formato adequado de um nome de chave ProgID é \[ *Vendor ou Application* \] . \[ *Componente* \] . \[ *Versão* \] , separada por períodos e sem espaços, como Word.Document.6. A *parte* Versão é opcional, mas altamente recomendada. Para obter mais informações, consulte [Usando identificadores programáticos com versão](#using-versioned-programmatic-identifiers).

Uma sub-chave ProgID deve incluir os elementos a seguir. Observe que alguns dados de cadeia de caracteres nessa chave exigem formatação específica.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>(Padrão)</strong></td>
<td>De definir a entrada padrão da sub-chave ProgID como um nome amigável para esse ProgID, adequado para exibição para o usuário. O uso dessa entrada para manter o nome amigável é preterido pela entrada FriendlyTypeName em sistemas que executam Windows 2000 ou posterior. No entanto, você deve definir esse valor para compatibilidade com backward.<br/></td>
</tr>
<tr class="even">
<td><strong>AllowSilentDefaultTakeOver</strong> (introduzido no Windows 8)</td>
<td>De definir essa entrada opcional para sinalizar Windows deve ignorar esse ProgID ao determinar um manipulador padrão para um tipo de arquivo público. Independentemente de esse valor ser definido, o ProgID continuará a aparecer no menu de atalho OpenWith e na caixa de diálogo. Esse é um REG_NONE valor.</td>
</tr>
<tr class="odd">
<td><strong>AppUserModelID</strong> (introduzido no Windows 7)</td>
<td>Defina essa entrada opcional como a ID explícita do modelo de usuário do aplicativo (AppUserModelID) se o aplicativo <strong></strong> usar <strong></strong> um AppUserModelID explícito e usar listas de salto recentes ou frequentes geradas automaticamente pelo sistema ou fornece um Lista de Atalhos. Se um aplicativo usar um AppUserModelID explícito e não definir esse valor, os itens não aparecerão nas Listas de Salto do aplicativo. Essa é uma cadeia REG_SZ cadeia de caracteres. Para obter mais informações, consulte IDs de modelo de usuário <a href="appids.md">do aplicativo (AppUserModelIDs)</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>EditFlags</strong></td>
<td>Defina essa entrada opcional usando sinalizadores da <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>enumeração FILETYPEATTRIBUTEFLAGS.</strong></a> A entrada EditFlags controla alguns aspectos da manipulação do Shell dos tipos de arquivo vinculados a esse ProgID. Você também pode usar a entrada EditFlags para limitar o quanto o usuário pode modificar determinados aspectos desses tipos de arquivo usando a folha de propriedades de um arquivo. Os <strong>valores FILETYPEATTRIBUTEFLAGS</strong> usados para EditFlags são valores binários projetados para que você possa combinar vários atributos em um único valor em uma operação OR bit a bit. Esse é um REG_DWORD ou REG_BINARY valor.<br/></td>
</tr>
<tr class="odd">
<td><strong>FriendlyTypeName</strong></td>
<td>De definir essa entrada como um nome amigável para o ProgID, adequado para exibição para o usuário. Para consistência, essa cadeia de caracteres deve conter os mesmos dados que a entrada Padrão para essa chave ProgID. Essa entrada pode ser uma cadeia de caracteres REG_SZ ou REG_EXPAND_SZ, mas deve ser formatada como uma cadeia de caracteres indireta (um nome de arquivo totalmente qualificado e valor de recurso precedido pelo símbolo @), por exemplo <em>, @%SystemRoot%\shell32.dll,-154</em>.<br/></td>
</tr>
<tr class="even">
<td><strong>InfoTip</strong></td>
<td>De definir essa entrada como uma breve mensagem de ajuda que o Shell exibe para este ProgID. A entrada InfoTip é exibida em uma caixa de diálogo de passar o mouse. Esse valor pode ser um REG_SZ ou REG_EXPAND_SZ cadeia de caracteres, mas, como FriendlyTypeName, ele deve ser formatado como uma cadeia de caracteres indireta.<br/></td>
</tr>
<tr class="odd">
<td><strong>CurVer</strong></td>
<td>De definir a entrada (Padrão) dessa sub-chave para a versão mais atual deste ProgID.<br/>
<blockquote>
[!Note]<br />
A menos que você tenha versões de aplicativo lado a lado, ou seja, várias versões instaladas no mesmo sistema, evite usar <strong>o CurVer</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>DefaultIcon</strong>.</td>
<td>De definir a entrada (Padrão) dessa sub-chave como o ícone padrão que você deseja exibir para tipos de arquivo associados a este ProgID. Esse valor pode ser uma cadeia de caracteres REG_SZ ou REG_EXPAND_SZ, mas deve ser fornecido como um nome de arquivo totalmente qualificado com seu valor de recurso de recurso de reserva, por exemplo <em>%SystemRoot%\shell32.dll,-154</em>.<br/></td>
</tr>
</tbody>
</table>



 

O exemplo de chave do Registro a seguir ilustra um nó de chave ProgID de associação de arquivo:

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a>Usando identificadores programáticos com versão

Um ProgID com versão é aquele cuja versão é indicada em seu nome. Normalmente, você faz isso adicionando um ponto e o número de versão ao nome. Por exemplo:

-   Word.Document.6
-   Word.Document.8

Esses são ProgIDs com versão, com as versões 6 e 8, respectivamente. Se você tiver um aplicativo lado a lado, ou seja, um que dá suporte a várias versões do seu aplicativo instaladas ao mesmo tempo, use CurVer e ProgIDs independentes de versão. Caso contrário, CurVer e ProgIDs independentes de versão devem ser evitados, pois eles levarão à ineficiência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como registrar um tipo de arquivo para um novo aplicativo](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[Registro de aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivos](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de Tipo de Arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Tipos percebidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 




