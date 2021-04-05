---
title: Interface ITsSbResourcePluginStoreEx
description: Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface ITsSbResourcePluginStoreEx
- Serviços de Área de Trabalho Remota da interface ITsSbResourcePluginStoreEx, descrita
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085761"
---
# <a name="itssbresourcepluginstoreex-interface"></a>Interface ITsSbResourcePluginStoreEx

Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos. Esses métodos adicionam, excluem e consultam esses objetos.

Essa interface só está disponível no Windows Server 2012 R2 com o [KB3091411](https://support.microsoft.com/kb/3091411) instalado. Os métodos [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) e [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) da interface [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) estão disponíveis a partir do Windows Server 2016.

## <a name="members"></a>Membros

A interface **ITsSbResourcePluginStoreEx** herda de [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore). **ITsSbResourcePluginStoreEx** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITsSbResourcePluginStoreEx** tem esses métodos.



| Método                                                                                                            | Descrição                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**AcquireTargetLock**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | Bloqueia um destino.<br/>                                                                                      |
| [**AddEnvironmentToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | Adiciona um ambiente ao armazenamento de plug-in de recurso.<br/>                                                   |
| [**AddSessionToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | Adiciona uma nova sessão ao armazenamento de plug-in de recurso.<br/>                                                    |
| [**AddTargetToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | Adiciona um destino ao armazenamento de plug-in de recurso.<br/>                                                         |
| [**DeleteTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | Exclui um destino.<br/>                                                                                    |
| [**EnumerateEnvironments**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | Retorna uma matriz que contém os ambientes presentes no repositório de plug-ins de recurso.<br/>               |
| [**EnumerateFarms**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | Enumera todos os farms que foram adicionados ao armazenamento de plug-in de recurso.<br/>                         |
| [**EnumerateSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | Enumera um conjunto de sessões especificado.<br/>                                                              |
| [**EnumerateTargets**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | Retorna uma matriz que contém os destinos especificados que estão presentes no repositório de plug-ins de recurso.<br/> |
| [**Getfarmproperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | Recupera uma propriedade de um farm.<br/>                                                                      |
| [**QueryEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | Retorna o objeto de ambiente especificado.<br/>                                                            |
| [**QuerySessionBySessionId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | Retorna o objeto de sessão que tem a ID de sessão especificada.<br/>                                        |
| [**QueryTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | Retorna o destino que tem o nome de destino e o nome do farm especificados.<br/>                                 |
| [**ReleaseTargetLock**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | Libera um bloqueio em um destino.<br/>                                                                         |
| [**RemoveEnvironmentFromStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | Remove o ambiente especificado do armazenamento de plug-in de recurso.<br/>                                   |
| [**SaveEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | Salva um ambiente.<br/>                                                                                |
| [**SaveSession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | Salva uma sessão.<br/>                                                                                     |
| [**SaveTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | Salva um destino.<br/>                                                                                      |
| [**Setenvironmentproperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | Define uma propriedade em um ambiente.<br/>                                                                   |
| [**SetEnvironmentPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | Define uma propriedade em um ambiente.<br/>                                                                   |
| [**Setsessionstate**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | Define o estado de uma sessão.<br/>                                                                         |
| [**SetTargetProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | Define uma propriedade em um destino.<br/>                                                                         |
| [**SetTargetPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | Define uma propriedade em um destino.<br/>                                                                         |
| [**Settargetstate**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | Define o estado de um destino.<br/>                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                             |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                                                             |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx é definido como 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[Interfaces de virtualização Área de Trabalho Remota](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





