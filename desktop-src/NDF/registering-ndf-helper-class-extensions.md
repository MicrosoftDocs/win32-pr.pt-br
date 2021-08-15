---
title: Registrando extensões de classe auxiliar NDF
description: Cada extensão de classe auxiliar tem um número de chaves do registro associadas a ela. Algumas chaves são exigidas pelo COM e algumas chaves são exigidas pelo NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e144abdeb1dbed1e33bb10e21302f918da8cdc5a6fd2090f3665e83f0316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798493"
---
# <a name="registering-ndf-helper-class-extensions"></a>Registrando extensões de classe auxiliar NDF

Cada extensão de classe auxiliar tem um número de chaves do registro associadas a ela. Algumas chaves são exigidas pelo COM e algumas chaves são exigidas pelo NDF.

## <a name="com-registry-keys"></a>Chaves do registro COM

Extensões de classe auxiliar devem ser implementadas como servidores COM. O registro COM deve ser concluído para cada extensão de classe auxiliar. O CLSID do objeto, a interface [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) e a interface [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) devem ser registrados. O registro cria um número de chaves do registro relacionadas COM para a extensão de classe auxiliar NDF.

## <a name="ndf-registry-keys"></a>Chaves do registro NDF

Extensões de classe auxiliar devem ser registradas antes de interagir com a estrutura de diagnóstico de rede e com outras classes auxiliares relacionadas. Isso é feito preenchendo o registro.

O procedimento a seguir mostra como adicionar extensões de classe auxiliar ao registro.

1.  Publique os nomes das classes auxiliares implementadas pela DLL e suas dependências criando uma chave para a DLL em

    **HKLM \\ Sistema \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *vendornamename* \\ **HostDLLs** \\ *auxiliar classe dll* \\ **HelperClasses** \\ *nome da classe auxiliar*

    Substitua *VendorName*, *dll de classe auxiliar* e *nome de classe auxiliar* por valores definidos pelo usuário, conforme descrito abaixo.

    | Valor               | Type    | Significado                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | REG \_ sz | O nome do fornecedor.                                                      |
    | *DLL de classe auxiliar*  | REG \_ sz | Nome da DLL, sem extensão.                                          |
    | *Nome da classe auxiliar* | REG \_ sz | O nome da classe auxiliar na qual a classe auxiliar atual é dependente. |

    

     

2.  Em cada chave de *nome de classe auxiliar* , publique as informações a seguir.

    

    | Valor         | Type       | Significado                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **CLSID**     | REG \_ sz    | Uma cadeia de caracteres que contém a ID de classe COM da classe auxiliar.                                                                                                            |
    | **Versão**   | REG \_ sz    | Uma cadeia de caracteres contém as versões principal e secundária da classe auxiliar no formato <major> <minor> .                                                        |
    | **Publicado** | REG \_ DWORD | Um valor de 1 significa que essa classe auxiliar deve ser invocada diretamente do cliente de diagnóstico. 0 significa que ele pode ser chamado somente de outra classe auxiliar. |
    | **Pai**    | REG \_ sz    | Uma cadeia de caracteres que nomeia a classe auxiliar extensível da Microsoft que está sendo estendida.                                                                                       |

    

     

3.  Para cada classe auxiliar, publique a lista de atributos correspondentes criando uma chave em

    **HKLM \\ Sistema \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *nome_do_fornecedorname* \\ **HostDLLs** \\ *auxiliar classe dll* \\ **HelperClasses** \\ *nome da classe auxiliar* \\ **matchattributes**

    A chave deve conter um ou mais valores (um por atributo) do seguinte tipo.

    | Valor             | Type                             | Significado                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | REG. reg do registro \_ \| \_ DWORD \| \_ | Um valor que conclui o par de nome e valor de um atributo específico. |

    

     

 

 




