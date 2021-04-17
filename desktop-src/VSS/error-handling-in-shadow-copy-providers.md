---
description: 'O VSS permite que muitas cópias de sombra existam de uma só vez, mas permite que uma criação de conjunto de cópias de sombra esteja em andamento entre a chamada para IVssBackupComponents:: StartSnapshotSet e o retorno da chamada para IVssBackupComponents::D oSnapshotSet.'
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Tratamento de erro em provedores de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f040526f63a0fe57fc5a49ac903e8b60b76646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751397"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Tratamento de erro em provedores de cópia de sombra

O VSS permite que muitas cópias de sombra existam de uma só vez, mas permite que uma criação de conjunto de cópias de sombra esteja em andamento entre a chamada para [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e o retorno da chamada para [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).

## <a name="no-partial-commit"></a>Nenhuma confirmação parcial

Se qualquer provedor falhar em uma cópia de sombra em qualquer volume ou LUN no conjunto de cópias de sombra, a criação do conjunto de cópias de sombra inteiro falhará. Isso ocorre por design. Esse design simplifica os problemas comportamentais associados à semântica de falha parcial e mantém um ponto no tempo consistente em todas as cópias de sombra do conjunto.

## <a name="reporting-fault-conditions"></a>Condições de falha de relatório

Se ocorrer um erro do provedor ou uma condição de falha, o provedor deverá registrar um erro no log de eventos do aplicativo. Isso inclui, mas não se limita a, quaisquer erros específicos de provedor ao criar ou importar um conjunto de cópias de sombra ou falha de alocação de recursos para cópia de sombra de cópia em gravação após a criação. Esse log não deve ocorrer durante o tempo em que os volumes no conjunto de cópias de sombra estão em um estado congelado.

## <a name="valid-provider-return-values"></a>Valores de retorno de provedor válidos

A tabela a seguir lista os códigos de retorno válidos para métodos de provedor e seus significados.



| Valor                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>S \_ OK<br/>                                                                                                                     | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ OUTOFMEMORY<br/>                                                                                          | O provedor está sem memória ou outros recursos do sistema.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | Um dos valores de parâmetro não é válido.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ ACCESSDENIED<br/>                                                                                       | Um cliente sem privilégios tentou chamar o provedor.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>VSS \_ E \_ estado inadequado \_<br/>                                                                                  | Nenhum provedor dá suporte à operação solicitada ou a operação não pode ser executada no objeto porque o objeto não está no estado correto.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>\_objeto VSS \_ E \_ não \_ encontrado<br/>                                                            | Um parâmetro refere-se a um objeto que não foi encontrado (como uma ID de cópia de sombra, ID de conjunto de cópias de sombra ou volume.)<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>VSS \_ E \_ armazenamento insuficiente \_<br/>                                                 | O provedor não pode executar a operação porque não há espaço em disco suficiente.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>VSS \_ E \_ volume \_ sem \_ suporte<br/>                                                | Nenhum provedor neste computador dá suporte à operação solicitada no volume.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>VSS \_ E \_ volume \_ sem \_ suporte \_ do \_ provedor<br/>          | O provedor não oferece suporte ao volume.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>VSS \_ E \_ \_ número máximo \_ de \_ instantâneos \_ atingidos<br/> | O provedor atingiu o número máximo de cópias de sombra que ele pode dar suporte.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>\_veto do \_ provedor \_ E do VSS<br/>                                                                      | O provedor encontrou um erro de tempo de execução interno que não é mapeado para outro valor de retorno. O provedor também deve gravar um evento no log de eventos do aplicativo, fornecendo ao usuário informações sobre como resolver esse problema.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E \_ não é possível \_ reverter \_ DiskId<br/>                                                | A assinatura MBR ou a ID GPT para um ou mais discos não pôde ser definida para o valor solicitado. Verifique o log de eventos do aplicativo para obter mais informações.<br/>                                                                                            |



 

O provedor não deve tentar retornar nenhum outro código de erro.

Se o provedor retornar um código de erro que não seja esperado (por exemplo, **S \_ false**, **\_ falhar**, **e \_ inesperado** ou **e \_ abortar**), o VSS gravará um evento no log de eventos mencionando o provedor e o método com falha e converterá o erro para o **VSS \_ E o \_ \_ \_ erro do provedor inesperado** antes de retornar ao solicitante. Isso não é feito para nenhum retorno de [**IVssProviderCreateSnapshotSet:: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) ou [**IVssProviderNotifications:: OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 




