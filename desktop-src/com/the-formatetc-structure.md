---
title: A estrutura FORMATETC
description: A estrutura FORMATETC é um formato de área de transferência generalizado, aprimorado para abranger um dispositivo de destino, um aspecto ou uma exibição dos dados e um meio de armazenamento.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641910"
---
# <a name="the-formatetc-structure"></a>A estrutura FORMATETC

A estrutura FORMATETC é um formato de área de transferência generalizado, aprimorado para abranger um dispositivo de destino, um *aspecto* ou uma exibição dos dados e um meio de armazenamento. Um consumidor de dados, como um aplicativo de contêiner OLE, passa a estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) como um argumento em chamadas para [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) para indicar o tipo de dados desejado de uma fonte de dados, como um objeto de documento composto. A origem usa a estrutura **FORMATETC** para descrever quais formatos ele pode fornecer.

O [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) pode descrever praticamente todos os dados, incluindo outros objetos, como monikers. Um contêiner pode pedir a um de seus objetos inseridos para listar seus formatos de dados chamando [**IDataObject:: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), que retorna um objeto enumerador que implementa a interface [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . Em vez de responder apenas que ele tem "texto e um bitmap", o objeto pode fornecer uma descrição detalhada dos dados, incluindo o dispositivo (normalmente a tela ou a impressora) para o qual ele é renderizado, o aspecto a ser apresentado ao usuário (conteúdo completo, miniatura, ícone ou formatado para impressão) e a mídia de armazenamento que contém os dados (memória global, arquivo de disco, objeto de armazenamento , ou Stream). Essa capacidade de descrever os dados de forma rígida, em tempo, resultará em uma impressão de qualidade e de saída de tela mais alta, bem como mais eficiência na navegação de dados, em que um esboço em miniatura é muito mais rápido de recuperar e exibir do que uma renderização totalmente detalhada.

A tabela a seguir lista os campos da estrutura de dados [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e as informações que eles especificam.



| Campo                   | Especifica                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | O formato no qual os dados serão renderizados, o que pode ser um formato de área de transferência padrão, um formato proprietário ou um formato OLE. Para obter mais informações sobre formatos OLE, consulte [documentos compostos](compound-documents.md).<br/>                                          |
| **ptd**<br/>      | Uma estrutura [**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) , que contém informações suficientes sobre um dispositivo de destino do Windows, como uma tela ou impressora, para que um identificador para seu contexto de dispositivo (HDC) possa ser criado usando a função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . <br/> |
| **dwAspect**<br/> | O aspecto ou a exibição dos dados a serem renderizados; pode ser o conteúdo completo, um esboço em miniatura, um ícone ou formatado para impressão.<br/>                                                                                                                                  |
| **lindex**<br/>   | A parte do aspecto que é interessante; para o presente, o valor deve ser-1, indicando que a exibição inteira é de interesse.<br/>                                                                                                                                |
| **tymed**<br/>    | O meio de armazenamento de dados, que pode ser memória global, arquivo de disco ou uma instância de uma das interfaces de armazenamento estruturado de COM.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de dados e mídia de transferência](data-formats-and-transfer-media.md)
</dt> </dl>

 

