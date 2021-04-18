---
description: A tabela de classes contém informações relacionadas ao servidor COM que devem ser geradas como parte do anúncio do produto. Cada linha pode gerar um conjunto de valores e chaves do registro. As informações de ProgId associadas estão incluídas nesta tabela.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabela de classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758968"
---
# <a name="class-table"></a>Tabela de classes

A tabela de classes contém informações relacionadas ao servidor COM que devem ser geradas como parte do anúncio do produto. Cada linha pode gerar um conjunto de valores e chaves do registro. As informações de ProgId associadas estão incluídas nesta tabela.

A tabela de classes tem as colunas a seguir.



| Coluna           | Tipo                         | Chave | Nullable |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | S   | N        |
| Contexto          | [Identificador](identifier.md) | S   | N        |
| Componente\_      | [Identificador](identifier.md) | S   | N        |
| ProgId \_ padrão  | [Text](text.md)             | N   | S        |
| Descrição      | [Text](text.md)             | N   | S        |
| AppId\_          | [GUID](guid.md)             | N   | S        |
| FileTypeMask     | [Text](text.md)             | N   | S        |
| ícone\_           | [Identificador](identifier.md) | N   | S        |
| IconIndex        | [Inteiro](integer.md)       | N   | S        |
| DefInprocHandler | [Filename](filename.md)     | N   | S        |
| Argumento         | [Binário](formatted.md)   | N   | S        |
| Recurso\_        | [Identificador](identifier.md) | N   | N        |
| Atributos       | [Inteiro](integer.md)       | N   | S        |



 

## <a name="column-information"></a>Informações da coluna

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

O identificador de classe (ID) de um servidor COM.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Noticioso
</dt> <dd>

O contexto do servidor para este servidor. Insira um dos valores a seguir para a chave CLSID.



| CHAVE CLSID                             | Descrição                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Especifica o caminho completo para um aplicativo de servidor local de 16 bits.             |
| [LocalServer32](../com/localserver32.md)   | Especifica o caminho completo para um aplicativo de servidor local de 32 bits.             |
| [InprocServer](../com/inprocserver.md)     | Especifica o caminho para uma DLL de servidor em processo.                           |
| [InprocServer32](../com/inprocserver32.md) | Especifica o caminho para um servidor em processo de 32 bits e o modelo de Threading. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na [tabela de componentes](component-table.md) especificando o componente cujo arquivo de chave fornece o servidor com.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ padrão
</dt> <dd>

A ID de programa padrão associada a essa ID de classe. Esta coluna é uma chave estrangeira na [tabela ProgID](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Descrição localizada associada à ID da classe e à ID do programa.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_
</dt> <dd>

ID do aplicativo que contém informações de DCOM para o aplicativo associado ( [GUID](guid.md)da cadeia de caracteres). Esta coluna é uma chave estrangeira na [tabela AppID](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Contém informações para a chave HKCR (esta CLSID).

Se existirem vários padrões, eles deverão ser delimitados por ponto e vírgula, e subchaves numéricas serão geradas: 0, 1, 2... Para obter mais informações sobre essa funcionalidade, consulte [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Cone\_
</dt> <dd>

O arquivo que fornece o ícone associado a este CLSID. O instalador grava a entrada nesta coluna sob a chave DefaultIcon associada ao ProgId. Se não for NULL, a coluna será uma chave estrangeira na tabela de [ícones](icon-table.md). Se for NULL, o servidor COM fornecerá o recurso de ícone. Associações de arquivo anunciadas e atalhos exigem um valor não nulo nesta coluna para serem exibidos corretamente.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice de ícone no arquivo de ícone. Isso pode ser nulo.

Somente números não negativos.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Este campo especifica o manipulador em processo padrão para o contexto de servidor especificado no campo de contexto.

Esse campo deverá ser nulo se uma chave CLSID InprocServer ou InprocServer aparecer no campo de contexto.

Se uma chave de CLSID LocalServer ou LocalServer32 aparecer no campo de contexto, o valor no campo DefInprocHandler identificará o manipulador em processo padrão.



| Valor                | Descrição                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| valor não numérico    | O instalador trata um valor não numérico no campo DefInprocHandler como um arquivo do sistema que serve como o manipulador de 32 bits no processo especificado pela chave InprocHandler32.                                                                                                            |
| Nulo                 | Os campos DefInprocHandler e Argument podem ser nulos para uma chave CLSID LocalServer ou LocalServer32.                                                                                                                                                                           |
| 1 = padrão (sistema) | O padrão é o manipulador no processo de 16 bits especificado por InprocHandler. Nesse caso, o valor de InprocHandler é o nome no registro sob o qual o valor do manipulador in-Process padrão é armazenado. Por exemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID.     |
| 2 = padrão (sistema) | O padrão é o manipulador no processo de 32 bits especificado por InprocHandler32. Nesse caso, o valor de InprocHandler32 é o nome no registro sob o qual o valor do manipulador in-Process padrão é armazenado. Por exemplo, HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID. |
| 3 = padrão (sistema) | O padrão é um manipulador no processo de 16 bits ou 32 bits.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Se uma chave de CLSID de LocalServer ou LocalServer32 aparecer no campo de contexto, o texto nesse campo será registrado como o argumento no servidor e será usado pelo COM para invocar o servidor. Os campos DefInprocHandler e Argument poderão ser nulos se LocalServer ou LocalServer32 aparecerem no campo de contexto.

Observe que a resolução das propriedades no campo argumento é limitada. Uma propriedade formatada como \[ propriedade \] nesse campo só poderá ser resolvida se a propriedade já tiver o valor pretendido quando o componente proprietário da classe for instalado. Por exemplo, para o argumento " \[ \#MyDoc.doc\] " para resolver o valor correto, o mesmo processo deve estar instalando o arquivo MyDoc.doc e o componente que possui a classe.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave externa na [tabela de recursos](feature-table.md) que especifica o recurso que fornece o servidor com.

Chave externa para a coluna um da tabela de recursos.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Se **msidbClassAttributesRelativePath** for definido nesta coluna, o nome de arquivo simples poderá ser usado para servidores com. O instalador registra o nome do arquivo somente em vez do caminho completo. Isso permite que o servidor no diretório atual tenha precedência e permita várias cópias do mesmo componente.



| Atributo                            | Decimal | Hexadecimal |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a [ação RegisterClassInfo](registerclassinfo-action.md) ou a [ação UnregisterClassInfo](unregisterclassinfo-action.md) é executada.

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

 

 
