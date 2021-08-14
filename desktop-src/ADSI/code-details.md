---
title: Detalhes do código
description: Esta seção lista o código-fonte para a implementação do componente do provedor de exemplo ADSI. Todas as referências de código-fonte neste documento estão sujeitas a alterações e estão disponíveis no diretório de código de exemplo incluído no SDK da ADSI.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- ADSI de Detalhes do Código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f03e7c7ed7d61d56f338a8bb44d51b1890d4bd24cd7dc1e6050f1900f6ff61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692282"
---
# <a name="code-details"></a>Detalhes do código

Esta seção lista o código-fonte para a implementação do componente do provedor de exemplo ADSI. Todas as referências de código-fonte neste documento estão sujeitas a alterações e estão disponíveis no diretório de código de exemplo incluído no SDK da ADSI.

> [!Note]  
> Os [**métodos IADs**](/windows/desktop/api/Iads/nn-iads-iads) **GetEx** e **PutEx** não são implementados no componente de provedor de exemplo ADSI. Ou seja, o código que implementa objetos do Active Directory herdados de **IADs** não tem **métodos GetEx** e **PutEx.** Isso inclui o objeto de classe de esquema que dá suporte a [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), o objeto de propriedade que dá suporte a [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), o objeto genérico do Active Directory que dá suporte a **IADs** e qualquer objeto de contêiner que dá suporte a [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Além disso, os objetos de sintaxe não estão presentes no componente do provedor de exemplo. No entanto, a arquitetura ADSI requer que os objetos de sintaxe sejam incluídos no objeto de contêiner de esquema, assim como os objetos de propriedade e classe de esquema.

 

A tabela a seguir lista os arquivos de código-fonte incluídos no diretório de exemplo do provedor no SDK de Interfaces de Serviço do Active Directory.



| Arquivo de código-fonte                 | Descrição                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj.cpp](cclsobj-cpp.md)   | Rotinas de objeto de classe de esquema.                                                                                                                                     |
| [cdispmgr.cpp](cdispmgr-cpp.md) | Implementação do Dispatch Manager.                                                                                                                                  |
| [cenumns.cpp](cenumns-cpp.md)   | Rotinas de enumeração de namespace.                                                                                                                                   |
| [cenumsch.cpp](cenumsch-cpp.md) | Rotinas de enumeração de esquema.                                                                                                                                      |
| [cenumobj.cpp](cenumobj-cpp.md) | Rotinas de enumeração de objeto genérico.                                                                                                                              |
| [cenumvar.cpp](cenumvar-cpp.md) | Implementação base para classes derivadas xxxEnumVariant.                                                                                                           |
| [cgenobj.cpp](cgenobj-cpp.md)   | Rotinas de objeto genérico.                                                                                                                                          |
| [cnamcf.cpp](cnamcf-cpp.md)     | Rotinas de fábrica de classe de namespace.                                                                                                                                 |
| [cnamesp.cpp](cnamesp-cpp.md)   | Rotinas de objeto de namespace.                                                                                                                                        |
| [common.cpp](common-cpp.md)     | Código comum a todos os objetos do provedor.                                                                                                                              |
| [core.cpp](core-cpp.md)         | Implementações para propriedades 'core' compartilhadas por todos os objetos do Active Directory.                                                                                     |
| [cprops.cpp](cprops-cpp.md)     | Recursos de cache de propriedade.                                                                                                                                          |
| [cprov.cpp](cprov-cpp.md)       | Rotinas de objeto do provedor de nível superior.                                                                                                                               |
| [cprovcf.cpp](cprovcf-cpp.md)   | Rotinas de fábrica de classe de objeto do provedor de nível superior.                                                                                                                 |
| [cprpobj.cpp](cprpobj-cpp.md)   | Rotinas de objeto de propriedade.                                                                                                                                         |
| [cschobj.cpp](cschobj-cpp.md)   | Rotinas de objeto de esquema.                                                                                                                                           |
| [getobj.cpp](getobj-cpp.md)     | Recurso GetObject.                                                                                                                                                |
| [globals.cpp](globals-cpp.md)   | Globales de componentes do provedor de exemplo ADSI.                                                                                                                          |
| [guid.cpp](guid-cpp.md)         | EXEMPLO de CLSIDs e LIBIDs do componente do provedor.                                                                                                                     |
| [libmain.cpp](libmain-cpp.md)   | Libmain para adssmp.dll.                                                                                                                                           |
| [memory.cpp](memory-cpp.md)     | Rotinas de gerenciamento de memória do componente do provedor de exemplo.                                                                                                            |
| [pack.cpp](pack-cpp.md)         | Exemplo de pacotes de componentes do provedor/desempacotar dados em VARIANTs.                                                                                                          |
| [parse.cpp](parse-cpp.md)       | Análise de caminho para o namespace de componente do provedor de exemplo.                                                                                                            |
| [property.cpp](property-cpp.md) | Obter e colocar propriedades por nome.                                                                                                                                   |
| [object.cpp](object-cpp.md)     | Exemplo de código de lista de tipos de objeto de componente do provedor para filtragem.                                                                                                   |
| [regdsapi.cpp](regdsapi-cpp.md) | APIs de serviço de diretório do registro de componente do provedor de exemplo.                                                                                                       |
| smpoper.cpp                      | Rotinas de conversão de dados.                                                                                                                                         |
| [stdfact.cpp](stdfact-cpp.md)   | Implementação [**padrão de IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)                                                                                                  |
| adssmp.inf                       | Dados de registro de armazenamento de dados de diretório de exemplo. Para obter mais informações, consulte [Instalando o componente provedor de exemplo](installing-the-example-provider-component.md). |



 

 

 