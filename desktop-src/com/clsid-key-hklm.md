---
title: Chave CLSID
description: Um CLSID é um identificador global exclusivo que identifica um objeto de classe COM. Se o servidor ou o contêiner permitir a vinculação a seus objetos inseridos, você precisará registrar um CLSID para cada classe de objetos com suporte.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- COM chave de Registro CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9253446a039e47996366c7dfdb51c01f9b1993
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364229"
---
# <a name="clsid-key"></a>Chave CLSID

Um CLSID é um identificador global exclusivo que identifica um objeto de classe COM. Se o servidor ou o contêiner permitir a vinculação a seus objetos inseridos, você precisará registrar um CLSID para cada classe de objetos com suporte.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_CLSID de \\ \\ classes de \\ software de computador local** \\ *{* CLSID *}*



| Chave do Registro                                                 | Descrição                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid.md)                                       | Associa um AppID a um CLSID.                                                                                                        |
| [**Converter autoconverteto**](autoconvertto.md)                       | Especifica a conversão automática de uma determinada classe de objetos em uma nova classe de objetos.                                                |
| [**Tratados autotratações**](autotreatas.md)                           | Define automaticamente o CLSID para a chave [**Treats**](treatas.md) para o valor especificado.                                              |
| [**AuxUserType**](auxusertype.md)                           | Especifica o nome de exibição curto de um aplicativo e os nomes de aplicativos.                                                                     |
| [**Control**](control.md)                                   | Identifica um objeto como um controle ActiveX.                                                                                              |
| [**Conversão**](conversion.md)                             | Usado pela caixa de diálogo **converter** para determinar os formatos que um aplicativo pode ler e gravar.                                           |
| [**Formatos de dataformativos**](dataformats.md)                           | Especifica os formatos de dados padrão e principal com suporte por um aplicativo.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Fornece informações de ícone padrão para icônico apresentações de objetos.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Especifica se um aplicativo usa um manipulador personalizado.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Especifica se um aplicativo usa um manipulador personalizado.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Especifica o caminho para a DLL do servidor em processo.                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | Registra um servidor em processo de 32 bits e especifica o modelo de Threading do apartamento no qual o servidor pode ser executado.                           |
| [**Insertable**](insertable.md)                             | Indica que os objetos dessa classe devem aparecer na caixa de listagem da caixa de diálogo **Inserir objeto** quando usados por aplicativos de contêiner com. |
| [**Interface**](interface.md)                               | Uma entrada opcional que especifica todas as IDs de interface (IIDs) com suporte pela classe associada.                                             |
| [**LocalServer**](localserver.md)                           | Especifica o caminho completo para um aplicativo de servidor local de 16 bits.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Especifica o caminho completo para um aplicativo de servidor local de 32 bits.                                                                            |
| [**MiscStatus**](miscstatus.md)                             | Especifica como criar e exibir um objeto.                                                                                           |
| [**ProgID**](progid.md)                                     | Associa um ProgID a um CLSID.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifica o nome do módulo e a ID de recurso para um bitmap de 16 x 16 a ser usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas.                      |
| [**Tratados**](treatas.md)                                   | Especifica o CLSID de uma classe que pode emular a classe atual.                                                                       |
| [**Verbo**](verb.md)                                         | Especifica os verbos a serem registrados para um aplicativo.                                                                                 |
| [**Versão**](version.md)                                   | Especifica o número de versão do controle.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Associa um ProgID a um CLSID. Esse valor é usado para determinar a versão mais recente de um aplicativo de objeto.                           |



 

## <a name="remarks"></a>Comentários

A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.

A chave CLSID contém informações usadas pelo manipulador COM padrão para retornar informações sobre uma classe quando ela estiver no estado executando.

Para obter um CLSID para seu aplicativo, você pode usar o Uuidgen.exe ou usar a função [**falha em CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .

O CLSID é um número de 128 bits, em Hex, dentro de um par de chaves.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Falha em CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




