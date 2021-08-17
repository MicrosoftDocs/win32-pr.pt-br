---
description: A tabela Classe contém informações relacionadas ao servidor COM que devem ser geradas como parte do anúncio do produto. Cada linha pode gerar um conjunto de chaves e valores do Registro. As informações de ProgId associadas estão incluídas nesta tabela.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabela de classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48985bd2d7e9670c89df53993e7170dc3e0e43a2b6e60f63d29e9f43e8d2ab3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066036"
---
# <a name="class-table"></a>Tabela de classes

A tabela Classe contém informações relacionadas ao servidor COM que devem ser geradas como parte do anúncio do produto. Cada linha pode gerar um conjunto de chaves e valores do Registro. As informações de ProgId associadas estão incluídas nesta tabela.

A tabela Classe tem as seguintes colunas.



| Coluna           | Tipo                         | Chave | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | Y   | N        |
| Contexto          | [Identificador](identifier.md) | Y   | N        |
| Componente\_      | [Identificador](identifier.md) | Y   | N        |
| Padrão \_ progId  | [Text](text.md)             | N   | Y        |
| Descrição      | [Text](text.md)             | N   | Y        |
| Appid\_          | [GUID](guid.md)             | N   | Y        |
| FileTypeMask     | [Text](text.md)             | N   | Y        |
| Ícone\_           | [Identificador](identifier.md) | N   | Y        |
| IconIndex        | [Inteiro](integer.md)       | N   | Y        |
| DefInprocHandler | [Filename](filename.md)     | N   | Y        |
| Argumento         | [Formatado](formatted.md)   | N   | Y        |
| Recurso\_        | [Identificador](identifier.md) | N   | N        |
| Atributos       | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>Informações da coluna

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>Clsid
</dt> <dd>

O ID (identificador de classe) de um servidor COM.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contexto
</dt> <dd>

O contexto do servidor para este servidor. Insira um dos valores a seguir para a Chave CLSID.



| CLSID KEY                             | Descrição                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Especifica o caminho completo para um aplicativo de servidor local de 16 bits.             |
| [LocalServer32](../com/localserver32.md)   | Especifica o caminho completo para um aplicativo de servidor local de 32 bits.             |
| [InprocServer](../com/inprocserver.md)     | Especifica o caminho para uma DLL de servidor em processo.                           |
| [Inprocserver32](../com/inprocserver32.md) | Especifica o caminho para um servidor em processo de 32 bits e o modelo de threading. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na tabela [Componente especificando](component-table.md) o componente cujo arquivo de chave fornece o servidor COM.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>Padrão \_ progId
</dt> <dd>

A ID do Programa padrão associada a essa ID de Classe. Essa coluna é uma chave estrangeira na [tabela ProgID](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrição
</dt> <dd>

Descrição localizada associada à ID da Classe e à ID do Programa.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>Appid\_
</dt> <dd>

ID do aplicativo que contém informações do DCOM para o aplicativo associado (GUID de cadeia de [caracteres).](guid.md) Essa coluna é uma chave estrangeira na [tabela AppId](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Contém informações para a chave HKCR (esta CLSID).

Se existirem vários padrões, eles deverão ser delimitados por um ponto e vírgula e sub-chaves numéricas serão geradas: 0, 1, 2... Para obter mais informações sobre essa funcionalidade, consulte [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Ícone\_
</dt> <dd>

O arquivo que fornece o ícone associado a este CLSID. O instalador grava a entrada nessa coluna na chave DefaultIcon associada à ProgId. Se não for nulo, a coluna será uma chave estrangeira na [tabela Ícone](icon-table.md). Se for nulo, o servidor COM fornece o recurso de ícone. Associações e atalhos de arquivo anunciados exigem um valor não nulo nesta coluna para ser exibido corretamente.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice de ícone no arquivo de ícone. Isso pode ser nulo.

Somente números não negativos.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Esse campo especifica o manipulador em processo padrão para o contexto do servidor especificado no campo Contexto.

Esse campo deverá ser Nulo se uma chave CLSID InprocServer ou InprocServer aparecer no campo Contexto.

Se uma chave CLSID LocalServer ou LocalServer32 for exibida no campo Contexto, o valor no campo DefInprocHandler identificará o manipulador padrão em processo.



| Valor                | Descrição                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valor não numérico    | O instalador trata um valor não numérico no campo DefInprocHandler como um arquivo do sistema que serve como o manipulador em processo de 32 bits especificado pela chave InprocHandler32.                                                                                                            |
| Nulo                 | Os campos DefInprocHandler e Argument podem ser Nulos para uma chave CLSID LocalServer ou LocalServer32.                                                                                                                                                                           |
| 1 = padrão (sistema) | O padrão é o manipulador em processo de 16 bits especificado por InprocHandler. Nesse caso, o valor de InprocHandler é o nome no registro no qual o valor do manipulador padrão em processo é armazenado. Por exemplo, CLSID de classes de SOFTWARE DE \_ MÁQUINA LOCAL \_ \\ \\ \\ HKEY.     |
| 2 = padrão (sistema) | O padrão é o manipulador em processo de 32 bits especificado por InprocHandler32. Nesse caso, o valor de InprocHandler32 é o nome no registro no qual o valor do manipulador padrão em processo é armazenado. Por exemplo, CLSID de classes de SOFTWARE DE \_ MÁQUINA LOCAL \_ \\ \\ \\ HKEY. |
| 3 = padrão (sistema) | O padrão é um manipulador em processo de 16 ou 32 bits.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Se uma chave CLSID LocalServer ou LocalServer32 aparecer no campo Contexto, o texto nesse campo será registrado como o argumento no servidor e será usado por COM para invocar o servidor. Os campos DefInprocHandler e Argument poderão ser Nulos se LocalServer ou LocalServer32 aparecerem no campo Contexto.

Observe que a resolução das propriedades no campo Argumento é limitada. Uma propriedade formatada como Propriedade nesse campo só poderá ser resolvida se a propriedade já tiver o valor pretendido quando o componente proprietário da \[ \] classe estiver instalado. Por exemplo, para o argumento "MyDoc.doc" para resolver para o valor correto, o mesmo processo deve estar instalando o arquivo MyDoc.doc e o componente que possui a \[ \# \] classe .

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave externa na tabela [Recurso especificando](feature-table.md) o recurso que fornece o servidor COM.

Chave externa para a coluna um da tabela Recurso.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Se **msidbClassAttributesRelativePath** for definido nesta coluna, o nome de arquivo simples poderá ser usado para servidores COM. O instalador registra o nome do arquivo somente em vez do caminho completo. Isso permite que o servidor no diretório atual tem precedência e permite várias cópias do mesmo componente.



| Atributo                            | Decimal | Hexadecimal |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referenciada quando a [ação RegisterClassInfo ou](registerclassinfo-action.md) [a ação UnregisterClassInfo](unregisterclassinfo-action.md) são executadas.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
