---
description: Depois que a fila for confirmada com êxito, você precisará atualizar as informações do registro para o produto que você está instalando.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Atualizando informações do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579ef64739bbe063d6fed19234a74b89b86b8b257793a1a26e83fd651256d189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683046"
---
# <a name="updating-registry-information"></a>Atualizando informações do registro

Depois que a fila for confirmada com êxito, você precisará atualizar as informações do registro para o produto que você está instalando. É recomendável aguardar até que todas as operações de cópia de arquivo necessárias tenham sido concluídas com êxito antes de alterar as informações do registro.

Uma maneira de atualizar o registro é chamar [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) com os \_ sinalizadores de INIFILES, registro mais giratório ou INI2REG de rotação mais fácil \_ \_ especificados. Esses sinalizadores podem ser combinados em uma chamada para **SetupInstallFromInfSection**.

O exemplo a seguir usa mais de \_ ^ arquivos de aceleração ^ \_ para indicar que a função deve processar todas as operações listadas, exceto as operações de arquivo. Como apenas as operações INI, registro e arquivo são listadas na seção **instalar** , esse é um método abreviado de especificar a função deve processar todas as operações ini e de registro.

O exemplo a seguir mostra como instalar informações de registro usando a função **SetupInstallFromINFSection** .

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

No exemplo, *OwnerWindow* é **nulo** porque apenas as operações de arquivo geram caixas de diálogo e, portanto, uma janela pai não é necessária. "MyInf" é o arquivo INF que contém a seção a ser processada. O parâmetro "MySection" especifica a seção a ser instalada. Os sinalizadores combinados, \_ todos os arquivos de rotação de ^ mais ^ \_ , especificam quais operações de instalação processar, nesse caso, todas as operações, exceto operações de arquivo. O caminho raiz de origem é especificado como "A: \\ ".

Como nenhuma operação de cópia está sendo processada, os parâmetros *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* e *DeviceInfoData* não são especificados.

 

 



