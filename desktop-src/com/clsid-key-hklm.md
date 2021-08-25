---
title: Chave CLSID
description: Um CLSID é um identificador global exclusivo que identifica um objeto de classe COM. Se o servidor ou contêiner permitir a vinculação a seus objetos inseridos, você precisará registrar um CLSID para cada classe de objetos com suporte.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- CHAVE DO Registro CLSID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd390fc6a1ccb15e128245c3b6a80e2b4ca57f41de9e9c21e93ebe4c708783d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854976"
---
# <a name="clsid-key"></a>Chave CLSID

Um CLSID é um identificador global exclusivo que identifica um objeto de classe COM. Se o servidor ou contêiner permitir a vinculação a seus objetos inseridos, você precisará registrar um CLSID para cada classe de objetos com suporte.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ CLASSES \_ DE SOFTWARE DE COMPUTADOR LOCAL \\ \\ \\ CLSID** \\ *{* CLSID *}*



| Chave do Registro                                                 | Descrição                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Appid**](appid.md)                                       | Associa um AppID a um CLSID.                                                                                                        |
| [**AutoConvertTo**](autoconvertto.md)                       | Especifica a conversão automática de uma determinada classe de objetos em uma nova classe de objetos .                                                |
| [**AutoTreatAs**](autotreatas.md)                           | Define automaticamente o CLSID para a [**chave TreatAs**](treatas.md) para o valor especificado.                                              |
| [**AuxUserType**](auxusertype.md)                           | Especifica o nome de exibição curto de um aplicativo e os nomes do aplicativo.                                                                     |
| [**Control**](control.md)                                   | Identifica um objeto como um controle ActiveX controle.                                                                                              |
| [**Conversão**](conversion.md)                             | Usado pela caixa **de diálogo** Converter para determinar os formatos que um aplicativo pode ler e gravar.                                           |
| [**Dataformats**](dataformats.md)                           | Especifica os formatos de dados padrão e principal com suporte de um aplicativo.                                                                 |
| [**Defaulticon**](defaulticon.md)                           | Fornece informações de ícone padrão para apresentações de objetos de exibição.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Especifica se um aplicativo usa um manipulador personalizado.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Especifica se um aplicativo usa um manipulador personalizado.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Especifica o caminho para a DLL do servidor em processo.                                                                                         |
| [**Inprocserver32**](inprocserver32.md)                     | Registra um servidor em processo de 32 bits e especifica o modelo de threading do apartment no qual o servidor pode executar.                           |
| [**Inserível**](insertable.md)                             | Indica que os objetos dessa classe devem aparecer na caixa de diálogo Inserir **Objeto** caixa de diálogo quando usados por aplicativos de contêiner COM. |
| [**Interface**](interface.md)                               | Uma entrada opcional que especifica todas as IDs de interface (IIDs) com suporte pela classe associada.                                             |
| [**LocalServer**](localserver.md)                           | Especifica o caminho completo para um aplicativo de servidor local de 16 bits.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Especifica o caminho completo para um aplicativo de servidor local de 32 bits.                                                                            |
| [**Miscstatus**](miscstatus.md)                             | Especifica como criar e exibir um objeto .                                                                                           |
| [**ProgID**](progid.md)                                     | Associa um ProgID a um CLSID.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifica o nome do módulo e a ID do recurso para um bitmap de 16 x 16 a ser usado para o rosto de uma barra de ferramentas ou botão de caixa de ferramentas.                      |
| [**Treatas**](treatas.md)                                   | Especifica o CLSID de uma classe que pode emular a classe atual.                                                                       |
| [**Verbo**](verb.md)                                         | Especifica os verbos a serem registrados para um aplicativo.                                                                                 |
| [**Versão**](version.md)                                   | Especifica o número de versão do controle.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Associa um ProgID a um CLSID. Esse valor é usado para determinar a versão mais recente de um aplicativo de objeto.                           |



 

## <a name="remarks"></a>Comentários

A **chave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde à chave **\_ \_ RAIZ de CLASSES HKEY,** que foi mantida para compatibilidade com versões anteriores do COM.

A chave CLSID contém informações usadas pelo manipulador COM padrão para retornar informações sobre uma classe quando ela está no estado de execução.

Para obter um CLSID para seu aplicativo, você pode usar o Uuidgen.exe ou usar a [**função CoCreateGuid.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)

O CLSID é um número de 128 bits, em hexa, dentro de um par de chaves.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Cocreateguid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




