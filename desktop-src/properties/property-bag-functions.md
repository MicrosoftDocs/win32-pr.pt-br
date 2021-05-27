---
description: Esta seção descreve um conjunto de funções auxiliares do Windows usadas com objetos IPropertyBag.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Funções de recipiente de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b694c579c76be96b00fa8392344ac59bdc0ce42f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550191"
---
# <a name="property-bag-functions"></a>Funções de recipiente de propriedades

Esta seção descreve um conjunto de funções auxiliares do Windows usadas com objetos [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) .



| Tópico                                                                       | Sumário                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ excluir**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Exclui uma propriedade de um recipiente de propriedades.<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Lê o valor de dados **bool** de uma propriedade em um recipiente de propriedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Lê um valor de dados **BSTR** de uma propriedade em um recipiente de propriedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Lê um valor de dados **DWORD** da propriedade em um recipiente de propriedades.<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Lê o valor de dados GUID de uma propriedade em um recipiente de propriedades.<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Lê um valor de dados **int** de uma propriedade em um recipiente de propriedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Lê um valor de dados **Long** de uma propriedade em um recipiente de propriedades.<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Recupera as coordenadas de propriedade armazenadas em uma estrutura [**pontual**](/previous-versions//dd162807(v=vs.85)) de um recipiente de propriedades especificado.<br/>    |
| [**PSPropertyBag \_ ReadPOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Recupera as coordenadas de propriedade armazenadas em uma [**estrutura POINTS**](/previous-versions//dd162808(v=vs.85)) de um pacote de propriedades especificado.<br/>    |
| [**PSPropertyBag \_ ReadPropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Lê a chave de propriedade de uma propriedade em um pacote de propriedades especificado.<br/>                                                 |
| [**ReadRECTL de PSPropertyBag \_**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Recupera as coordenadas de um retângulo armazenado em uma propriedade contida em um pacote de propriedades especificado.<br/>              |
| [**ReadSHORT de PSPropertyBag \_**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Lê o valor **de dados SHORT** de uma propriedade em um pacote de propriedades.<br/>                                                   |
| [**ReadStr de PSPropertyBag \_**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Lê o valor de **dados da** cadeia de caracteres de uma propriedade em um pacote de propriedades.<br/>                                                  |
| [**PSPropertyBag \_ ReadStrAlloc**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Lê um valor **de dados de** cadeia de caracteres de uma propriedade em um pacote de propriedades e aloca memória para a cadeia de caracteres lida.<br/> |
| [**PSPropertyBag \_ ReadStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Lê o fluxo de dados armazenado em uma determinada propriedade contida em um pacote de propriedades especificado.<br/>                           |
| [**PSPropertyBag \_ ReadType**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Lê o tipo de valor de dados de uma propriedade armazenada em um pacote de propriedades.<br/>                                      |
| [**PSPropertyBag \_ ReadULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Lê um valor **de dados ULONGLONG** de uma propriedade em um pacote de propriedades.<br/>                                               |
| [**PSPropertyBag \_ ReadUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Lê uma determinada propriedade de um valor de dados desconhecido em um pacote de propriedades.<br/>                                                |
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Define o valor de dados **bool** de uma propriedade em um recipiente de propriedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Define um valor de dados **BSTR** de uma propriedade em um recipiente de propriedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Define um valor de dados **DWORD** da propriedade em um recipiente de propriedades.<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Define o valor dos dados GUID de uma propriedade em um recipiente de propriedades.<br/>                                                       |
| [**PSPropertyBag \_ WriteInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Define um valor de dados **int** de uma propriedade em um recipiente de propriedades.<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Define um valor de dados **Long** de uma propriedade em um recipiente de propriedades.<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Armazena as coordenadas de propriedade armazenadas em uma estrutura [**pontual**](/previous-versions//dd162807(v=vs.85)) de um recipiente de propriedades especificado.<br/>       |
| [**PSPropertyBag \_ WritePOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Armazena as coordenadas de propriedade armazenadas em uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) de um recipiente de propriedades especificado.<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Define a chave de propriedade de uma propriedade em um recipiente de propriedades especificado.<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Armazena as coordenadas de um retângulo armazenado em uma propriedade contida em um recipiente de propriedades especificado.<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Define o **valor de** dados SHORT de uma propriedade em um pacote de propriedades.<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Define o valor **de dados** da cadeia de caracteres de uma propriedade em um pacote de propriedades.<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Define o fluxo de dados armazenado em uma determinada propriedade contida em um pacote de propriedades especificado.<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Define um **valor de dados ULONGLONG** de uma propriedade em um pacote de propriedades.<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Define uma determinada propriedade de um valor de dados desconhecido em um pacote de propriedades.<br/>                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções PROPVARIANT e VARIANT](./functions-propvarutil.md)
</dt> <dt>

[Funções](functions.md)
</dt> </dl>

 

 
