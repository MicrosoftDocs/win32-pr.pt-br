---
title: Detalhes do código
description: Esta seção lista o código-fonte para a implementação do componente do provedor de exemplo ADSI. Todas as referências de código-fonte neste documento estão sujeitas a alterações e estão disponíveis no diretório de código de exemplo incluído no SDK do ADSI.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- ADSI de detalhes de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d959357f2cdd094b26cde4f649c3286389b8415
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008356"
---
# <a name="code-details"></a>Detalhes do código

Esta seção lista o código-fonte para a implementação do componente do provedor de exemplo ADSI. Todas as referências de código-fonte neste documento estão sujeitas a alterações e estão disponíveis no diretório de código de exemplo incluído no SDK do ADSI.

> [!Note]  
> Os [](/windows/desktop/api/Iads/nn-iads-iads) métodos IADs **GetEx** e **PutEx** não são implementados no componente de provedor de exemplo ADSI. Ou seja, o código que implementa Active Directory objetos que herdam de **IADs** não têm os métodos **GetEx** e **PutEx** . Isso inclui o objeto de classe de esquema que dá suporte a [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), o objeto Property que dá suporte a [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), o objeto Active Directory genérico que dá suporte a **IADs** e qualquer objeto de contêiner que dá suporte a [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Além disso, os objetos de sintaxe não estão presentes no componente de provedor de exemplo. No entanto, a arquitetura ADSI exige que os objetos de sintaxe sejam incluídos no objeto contêiner de esquema, assim como os objetos classe de esquema e propriedade.

 

A tabela a seguir lista os arquivos de código-fonte que são incluídos no diretório de exemplo do provedor no SDK do Active Directory Service Interfaces.



| Arquivo de código-fonte                 | Descrição                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj. cpp](cclsobj-cpp.md)   | Rotinas de objeto de classe de esquema.                                                                                                                                     |
| [cdispmgr. cpp](cdispmgr-cpp.md) | Implementação do Gerenciador de expedição.                                                                                                                                  |
| [cenumns. cpp](cenumns-cpp.md)   | Rotinas de enumeração de namespace.                                                                                                                                   |
| [cenumsch. cpp](cenumsch-cpp.md) | Rotinas de enumeração de esquema.                                                                                                                                      |
| [cenumobj. cpp](cenumobj-cpp.md) | Rotinas de enumeração de objeto genérico.                                                                                                                              |
| [cenumvar. cpp](cenumvar-cpp.md) | Implementação de base para classes derivadas de xxxEnumVariant.                                                                                                           |
| [cgenobj. cpp](cgenobj-cpp.md)   | Rotinas de objeto genérico.                                                                                                                                          |
| [cnamcf. cpp](cnamcf-cpp.md)     | Rotinas de fábrica de classes de namespace.                                                                                                                                 |
| [cnamesp. cpp](cnamesp-cpp.md)   | Rotinas de objeto de namespace.                                                                                                                                        |
| [Common. cpp](common-cpp.md)     | Código comum a todos os objetos de provedor.                                                                                                                              |
| [Core. cpp](core-cpp.md)         | Implementações para Propriedades ' Core ' compartilhadas por todos os objetos de Active Directory.                                                                                     |
| [cProps. cpp](cprops-cpp.md)     | Recursos de cache de propriedade.                                                                                                                                          |
| [cprov. cpp](cprov-cpp.md)       | Rotinas de objeto de provedor de nível superior.                                                                                                                               |
| [cprovcf. cpp](cprovcf-cpp.md)   | Rotinas de fábrica da classe de objeto do provedor de nível superior.                                                                                                                 |
| [cprpobj. cpp](cprpobj-cpp.md)   | Rotinas de objeto de propriedade.                                                                                                                                         |
| [cschobj. cpp](cschobj-cpp.md)   | Rotinas de objeto de esquema.                                                                                                                                           |
| [getobj. cpp](getobj-cpp.md)     | Recurso GetObject.                                                                                                                                                |
| [Globals. cpp](globals-cpp.md)   | Globais do componente do provedor de exemplo ADSI.                                                                                                                          |
| [GUID. cpp](guid-cpp.md)         | CLSIDs de componente de provedor de exemplo e LIBIDs.                                                                                                                     |
| [LibMain. cpp](libmain-cpp.md)   | LibMain para adssmp.dll.                                                                                                                                           |
| [Memory. cpp](memory-cpp.md)     | Rotinas de gerenciamento de memória de componente de provedor de exemplo.                                                                                                            |
| [Pack. cpp](pack-cpp.md)         | Exemplo de pacote de componente de provedor/desempacotamento de dados em VARIAntes.                                                                                                          |
| [Parse. cpp](parse-cpp.md)       | Análise de caminho para o exemplo de namespace de componente de provedor.                                                                                                            |
| [Property. cpp](property-cpp.md) | Obter e colocar Propriedades por nome.                                                                                                                                   |
| [Object. cpp](object-cpp.md)     | Exemplo de código de tipo de objeto componente de provedor para filtragem.                                                                                                   |
| [regdsapi. cpp](regdsapi-cpp.md) | Exemplo de APIs de serviço de diretório do registro de componente do provedor.                                                                                                       |
| smpoper. cpp                      | Rotinas de conversão de dados.                                                                                                                                         |
| [stdfact. cpp](stdfact-cpp.md)   | Implementação de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) padrão.                                                                                                  |
| adssmp. inf                       | Exemplo de dados de registro de armazenamento de dados de diretório. Para obter mais informações, consulte [instalando o componente de provedor de exemplo](installing-the-example-provider-component.md). |



 

 

 