---
description: Objeto de Destino
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Objeto de Destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b528d66fb789e4d237dacae151c3dda596e834f84f529c3677905672de3b7588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057944"
---
# <a name="target-object"></a>Objeto de Destino

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de destino modela um destino iSCSI que está contido em um subsistema iSCSI.

Use o método [**IVdsSubSystemIscsi:: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) para determinar os destinos iSCSI do subsistema. Os chamadores podem obter um ponteiro para um destino específico selecionando o objeto de destino desejado da enumeração que é retornada pelo método **QueryTargets** . Com um objeto de destino, você pode definir o nome amigável e a consulta do destino para propriedades de destino, LUNs associados e o subsistema que contém o destino.

Os computadores host devem fazer logon nos destinos para acessar seus LUNs associados. Para executar um logon em um destino, o destino deve ter pelo menos um portal associado em um de seus grupos de Portal. A entrada e a saída de LUNs associados são manipuladas por meio desta sessão de logon.

As propriedades do objeto de destino incluem um identificador de objeto, um nome de iSCSI, um nome amigável e um sinalizador habilitado para CHAP.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0 | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Enumerações associadas                                                                   | Nenhum.                                                                                                                       |
| Estruturas associadas                                                                     | [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) Notificação de destino do [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_target_notification)e da prop de destino iSCSI. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
