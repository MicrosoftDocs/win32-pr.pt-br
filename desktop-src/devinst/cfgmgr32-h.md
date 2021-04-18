---
title: 'Cfgmgr32.h '
description: Esta seção contém tópicos de referência para o cabeçalho Cfgmgr32. h.
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ccc2baf458fea5e20842c9bfa60028c2cb8e23
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105753203"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h 

Esta seção contém tópicos de referência para o cabeçalho Cfgmgr32. h.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>A estrutura de BUSNUMBER_DES é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de números de barramento para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>A estrutura de BUSNUMBER_RANGE especifica uma lista de requisitos de recursos que descreve o uso de números de barramento para uma instância de dispositivo. Para obter mais informações sobre as listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>A estrutura de BUSNUMBER_RESOURCE especifica uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de números de barramento para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td>A função <strong>CM_Add_Empty_Log_Conf</strong> cria uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a>vazia, para um tipo de configuração especificado e uma instância de dispositivo especificada, no computador local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> .
</blockquote>
<br/> A função <strong>CM_Add_Empty_Log_Conf_Ex</strong> cria uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a>vazia, para um tipo de configuração especificado e uma instância de dispositivo especificada, no computador local ou remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td>A função <strong>CM_Add_ID</strong> acrescenta uma ID de <a href="/windows-hardware/drivers/install/device-ids">dispositivo</a> especificada (se ainda não estiver presente) a uma lista de <a href="/windows-hardware/drivers/install/hardware-ids">ID de hardware</a> ou lista de <a href="/windows-hardware/drivers/install/compatible-ids">IDs compatível</a> <a href="/windows-hardware/drivers/">da instância do dispositivo</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> .
</blockquote>
<br/> A função <strong>CM_Add_ID_Ex</strong> acrescenta uma <a href="/windows-hardware/drivers/install/device-ids">ID de dispositivo</a> (se ainda não estiver presente) à lista de ID de <a href="/windows-hardware/drivers/install/hardware-ids">hardware</a> ou à lista de ID <a href="/windows-hardware/drivers/install/compatible-ids">compatível</a> de uma instância de dispositivo, no computador local ou remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td>A função <strong>CM_Add_Res_Des</strong> adiciona um <a href="/windows-hardware/drivers/">descritor de recurso</a> a uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> .
</blockquote>
<br/> A função <strong>CM_Add_Res_Des_Ex</strong> adiciona um <a href="/windows-hardware/drivers/">descritor de recurso</a> a uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a>. A configuração lógica pode estar no computador local ou remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, a funcionalidade para acessar máquinas remotas foi removida. Não é possível acessar computadores remotos durante a execução nessas versões do Windows.
</blockquote>
<br/> A função <strong>CM_Connect_Machine</strong> cria uma conexão com um computador remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td>A função <strong>CM_Delete_Class_Key</strong> remove a classe de <a href="/windows-hardware/drivers/">dispositivo</a> instalada especificada do sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td>A função <strong>CM_Delete_Device_Interface_Key</strong> exclui a subchave do Registro usada por aplicativos e drivers para armazenar informações específicas da interface.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> A função <strong>CM_Delete_Device_Interface_Key_ExA</strong> exclui a subchave do Registro usada por aplicativos e drivers para armazenar informações específicas da interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> A função <strong>CM_Delete_Device_Interface_Key_ExW</strong> exclui a subchave do Registro usada por aplicativos e drivers para armazenar informações específicas da interface.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td>A função <strong>CM_Delete_DevNode_Key</strong> exclui as chaves do registro especificadas pelo usuário que estão associadas a um dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td>A função <strong>CM_Disable_DevNode</strong> desabilita um dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, a funcionalidade para acessar máquinas remotas foi removida. Não é possível acessar computadores remotos durante a execução nessas versões do Windows.
</blockquote>
<br/> A função <strong>CM_Disconnect_Machine</strong> remove uma conexão com um computador remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td>A função <strong>CM_Enable_DevNode</strong> habilita um dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>A função <strong>CM_Enumerate_Classes</strong> , quando chamada repetidamente, enumera as <a href="/windows-hardware/drivers/">classes de dispositivo</a> instaladas do computador local fornecendo o GUID de cada classe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> .
</blockquote>
<br/> A função <strong>CM_Enumerate_Classes_Ex</strong> , quando chamada repetidamente, enumera as <a href="/windows-hardware/drivers/">classes de dispositivo</a>instaladas ou locais de um computador remoto, fornecendo o GUID de cada classe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td>A função <strong>CM_Enumerate_Enumerators</strong> enumera enumeradores de dispositivo do computador local fornecendo o nome de cada enumerador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> .
</blockquote>
<br/> A função <strong>CM_Enumerate_Enumerators_Ex</strong> enumera enumeradores de dispositivo de um computador local ou remoto, fornecendo o nome de cada enumerador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td>A função <strong>CM_Free_Log_Conf</strong> remove uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> e todos os <a href="/windows-hardware/drivers/">descritores de recursos</a> associados do computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> .
</blockquote>
<br/> A função <strong>CM_Free_Log_Conf_Ex</strong> remove uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> e todos os <a href="/windows-hardware/drivers/">descritores de recursos</a> associados de um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td>A função <strong>CM_Free_Log_Conf_Handle</strong> invalida um identificador de configuração lógica e libera sua alocação de memória associada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td>A função <strong>CM_Free_Res_Des</strong> remove um <a href="/windows-hardware/drivers/">descritor de recurso</a> de uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> no computador local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> .
</blockquote>
<br/> A função <strong>CM_Free_Res_Des_Ex</strong> remove um <a href="/windows-hardware/drivers/">descritor de recurso</a> de uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> em um computador local ou remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td>A função <strong>CM_Free_Res_Des_Handle</strong> invalida um identificador de descrição de recurso e libera sua alocação de memória associada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td>A função <strong>CM_Free_Resource_Conflict_Handle</strong> invalida um identificador para uma lista de conflitos de recursos e libera a alocação de memória associada do identificador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td>A função <strong>CM_Get_Child</strong> é usada para recuperar um identificador de instância de dispositivo para o primeiro nó filho de um nó de dispositivo especificado (<a href="/windows-hardware/drivers/">Devnode</a>) na <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivos</a>do computador local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Child_Ex</strong> é usada para recuperar um identificador de instância de dispositivo para o primeiro nó filho de um nó de dispositivo especificado (<a href="/windows-hardware/drivers/">Devnode</a>) em uma <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivo</a>local ou de máquina remota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td>A função <strong>CM_Get_Class_Property</strong> recupera uma propriedade de dispositivo que é definida para uma classe de <a href="/windows-hardware/drivers/install/device-interface-classes">interface de dispositivo</a> ou classe de instalação de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Class_Property_ExW</strong> recupera uma propriedade de dispositivo que é definida para uma classe de <a href="/windows-hardware/drivers/install/device-interface-classes">interface de dispositivo</a> ou classe de instalação de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td>A função <strong>CM_Get_Class_Property_Keys</strong> recupera uma matriz das chaves de Propriedade do dispositivo que representam as propriedades do dispositivo que são definidas para uma classe de <a href="/windows-hardware/drivers/install/device-interface-classes">interface</a> de dispositivo ou classe de <a href="/windows-hardware/drivers/install/device-setup-classes">instalação de dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Class_Property_Keys_Ex</strong> recupera uma matriz das chaves de Propriedade do dispositivo que representam as propriedades do dispositivo que são definidas para uma classe de <a href="/windows-hardware/drivers/install/device-interface-classes">interface</a> de dispositivo ou classe de <a href="/windows-hardware/drivers/install/device-setup-classes">instalação de dispositivo</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td>A função <strong>CM_Get_Class_Registry_Property</strong> recupera uma <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">propriedade de classe de instalação de dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td>A função <strong>CM_Get_Depth</strong> é usada para obter a profundidade de um nó de dispositivo especificado (<a href="/windows-hardware/drivers/">Devnode</a>) na <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivo</a>do computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Depth_Ex</strong> é usada para obter a profundidade de um nó de dispositivo especificado (<a href="/windows-hardware/drivers/">Devnode</a>) em uma <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivo</a>local ou de máquina remota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_ID</strong> recupera a <a href="/windows-hardware/drivers/install/device-instance-ids">ID da instância do dispositivo</a> para uma <a href="/windows-hardware/drivers/">instância de dispositivo</a> especificada no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Device_ID_Ex</strong> recupera a <a href="/windows-hardware/drivers/install/device-instance-ids">ID da instância do dispositivo</a> para uma <a href="/windows-hardware/drivers/">instância de dispositivo</a> especificada em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_ID_List</strong> recupera uma lista de <a href="/windows-hardware/drivers/install/device-instance-ids">IDs de instância de dispositivo</a> para as <a href="/windows-hardware/drivers/">instâncias de dispositivo</a>do computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Device_ID_List_Ex</strong> recupera uma lista de <a href="/windows-hardware/drivers/install/device-instance-ids">IDs de instância de dispositivo</a> para as <a href="/windows-hardware/drivers/">instâncias de dispositivo</a> em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_ID_List_Size</strong> recupera o tamanho do buffer necessário para manter uma lista de <a href="/windows-hardware/drivers/install/device-instance-ids">IDs de instância de dispositivo</a> para as <a href="/windows-hardware/drivers/">instâncias de dispositivo</a>do computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Device_ID_List_Size_Ex</strong> recupera o tamanho do buffer necessário para manter uma lista de <a href="/windows-hardware/drivers/install/device-instance-ids">IDs de instância de dispositivo</a> para as instâncias de <a href="/windows-hardware/drivers/">dispositivo</a>de um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_ID_Size</strong> recupera o tamanho do buffer necessário para manter uma <a href="/windows-hardware/drivers/install/device-instance-ids">ID de instância de dispositivo</a> para uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Device_ID_Size_Ex</strong> recupera o tamanho do buffer necessário para manter uma <a href="/windows-hardware/drivers/install/device-instance-ids">ID de instância de dispositivo</a> para uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_Interface_Alias</strong> retorna o alias da instância de interface de dispositivo especificada, se o alias existir.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_Interface_List</strong> recupera uma lista de instâncias de interface de dispositivo que pertencem a uma <a href="/windows-hardware/drivers/install/device-interface-classes">classe de interface de dispositivo</a>especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_Interface_List_Size</strong> recupera o tamanho do buffer que deve ser passado para a função <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_Interface_Property</strong> recupera uma propriedade de dispositivo que é definida para uma interface de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Device_Interface_Property_ExW</strong> recupera uma propriedade de dispositivo que é definida para uma interface de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td>A função <strong>CM_Get_Device_Interface_Property_Keys</strong> recupera uma matriz de chaves de Propriedade do dispositivo que representam as propriedades do dispositivo que são definidas para uma interface de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong> recupera uma matriz de chaves de Propriedade do dispositivo que representam as propriedades do dispositivo que são definidas para uma interface de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td>A função <strong>CM_Get_DevNode_Property</strong> recupera uma propriedade de instância de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_DevNode_Property_ExW</strong> recupera uma propriedade de instância de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td>A função <strong>CM_Get_DevNode_Property_Keys</strong> recupera uma matriz das chaves de Propriedade do dispositivo que representam as propriedades do dispositivo que são definidas para uma instância do dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_DevNode_Property_Keys_Ex</strong> recupera uma matriz das chaves de Propriedade do dispositivo que representam as propriedades do dispositivo que são definidas para uma instância do dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td>A função <strong>CM_Get_DevNode_Registry_Property</strong> recupera uma propriedade de dispositivo especificada do registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td>A função <strong>CM_Get_DevNode_Status</strong> Obtém o status de uma instância de dispositivo do nó do dispositivo (<a href="/windows-hardware/drivers/">DevNode</a>) na <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivo</a>do computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_DevNode_Status_Ex</strong> Obtém o status de uma instância de dispositivo do nó do dispositivo (<a href="/windows-hardware/drivers/">DevNode</a>) em uma <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivo</a>local ou de máquina remota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td>A função <strong>CM_Get_First_Log_Conf</strong> Obtém a primeira <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a>de um tipo de configuração especificado, associada a uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> especificada no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_First_Log_Conf_Ex</strong> Obtém a primeira <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> associada a uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> especificada em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida e não deve ser usada.
</blockquote>
<br/> A função <strong>CM_Get_HW_Prof_Flags</strong> recupera os sinalizadores de configuração específicos do <a href="/windows-hardware/drivers/">perfil de hardware</a>para uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> em um computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função foi preterida e não deve ser usada.
</blockquote>
<br/> A função <strong>CM_Get_HW_Prof_Flags_Ex</strong> recupera os sinalizadores de configuração específicos do <a href="/windows-hardware/drivers/">perfil de hardware</a>para uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> em um computador remoto ou em um computador local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td>A função <strong>CM_Get_Log_Conf_Priority</strong> Obtém a prioridade de configuração de uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> especificada no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Log_Conf_Priority_Ex</strong> Obtém a prioridade de configuração de uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> especificada em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td>A função <strong>CM_Get_Next_Log_Conf</strong> Obtém a próxima <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> associada a uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> específica no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Next_Log_Conf_Ex</strong> Obtém a próxima <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> associada a uma instância de <a href="/windows-hardware/drivers/">dispositivo</a> específica em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td>A função <strong>CM_Get_Next_Res_Des</strong> Obtém um identificador para o próximo <a href="/windows-hardware/drivers/">descritor de recurso</a>, de um tipo de recurso especificado, para uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Next_Res_Des_Ex</strong> Obtém um identificador para o próximo <a href="/windows-hardware/drivers/">descritor de recurso</a>, de um tipo de recurso especificado, para uma <a href="/windows-hardware/drivers/kernel/hardware-resources">configuração lógica</a> em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td>A função <strong>CM_Get_Parent</strong> Obtém um identificador de instância de dispositivo para o nó pai de um nó de dispositivo especificado (<a href="/windows-hardware/drivers/">Devnode</a>) na árvore de dispositivo do computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Parent_Ex</strong> Obtém um identificador de instância de dispositivo para o nó pai de um nó de dispositivo especificado (<a href="/windows-hardware/drivers/">Devnode</a>) em uma <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivo</a>local ou de máquina remota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td>A função <strong>CM_Get_Res_Des_Data</strong> recupera as informações armazenadas em um <a href="/windows-hardware/drivers/">descritor de recurso</a> no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Res_Des_Data_Ex</strong> recupera as informações armazenadas em um <a href="/windows-hardware/drivers/">descritor de recurso</a> em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td>A função <strong>CM_Get_Res_Des_Data_Size</strong> Obtém o tamanho do buffer necessário para manter as informações contidas em um <a href="/windows-hardware/drivers/">descritor de recurso</a> especificado no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Res_Des_Data_Size_Ex</strong> Obtém o tamanho do buffer necessário para manter as informações contidas em um <a href="/windows-hardware/drivers/">descritor de recurso</a> especificado em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td>A função <strong>CM_Get_Resource_Conflict_Count</strong> Obtém o número de conflitos contidos em uma lista de conflitos de recursos especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td>A função <strong>CM_Get_Resource_Conflict_Details</strong> Obtém os detalhes sobre um dos conflitos de recurso em uma lista de conflitos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td>A função <strong>CM_Get_Sibling</strong> Obtém um identificador de instância de dispositivo para o próximo nó irmão de um nó de dispositivo especificado (<a href="/windows-hardware/drivers/">Devnode</a>) na árvore de <a href="/windows-hardware/drivers/kernel/device-tree">dispositivo</a>do computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> .
</blockquote>
<br/> A função <strong>CM_Get_Sibling_Ex</strong> Obtém um identificador de instância de dispositivo para o próximo nó irmão de um nó de dispositivo especificado, em uma <a href="/windows-hardware/drivers/kernel/device-tree">árvore de dispositivo</a>local ou de máquina remota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida e não deve ser usada.
</blockquote>
<br/> A função <strong>CM_Get_Version</strong> retorna a versão 4,0 do plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) para um computador local. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida e não deve ser usada.
</blockquote>
<br/> A função <strong>CM_Get_Version_Ex</strong> retorna a versão 4,0 do plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) para um computador local ou remoto. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td>A função <strong>CM_Is_Dock_Station_Present</strong> identifica se uma <a href="/windows-hardware/drivers/">estação de encaixe</a> está presente em um computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> .
</blockquote>
<br/> A função <strong>CM_Is_Dock_Station_Present_Ex</strong> identifica se uma <a href="/windows-hardware/drivers/">estação de encaixe</a> está presente em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida e não deve ser usada.
</blockquote>
<br/> A função <strong>CM_Is_Version_Available</strong> indica se uma versão especificada do plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) é suportada por um computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida e não deve ser usada.
</blockquote>
<br/> A função <strong>CM_Is_Version_Available_Ex</strong> indica se uma versão especificada do plug and Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) é suportada por um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td>A função <strong>CM_Locate_DevNode</strong> Obtém um identificador de instância de dispositivo para o nó de dispositivo que está associado a uma <a href="/windows-hardware/drivers/install/device-instance-ids">ID de instância de dispositivo</a> especificada no computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> .
</blockquote>
<br/> A função <strong>CM_Locate_DevNode_Ex</strong> Obtém um identificador de instância de dispositivo para o nó de dispositivo que está associado a uma <a href="/windows-hardware/drivers/install/device-instance-ids">ID de instância de dispositivo</a>especificada, em um computador local ou em um computador remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>Converte um código <strong>CONFIGRET</strong> especificado em seu código de erro do sistema equivalente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td>A função <strong>CM_Modify_Res_Des</strong> modifica um descritor de recurso especificado no computador local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> .
</blockquote>
<br/> A função <strong>CM_Modify_Res_Des_Ex</strong> modifica um descritor de recurso especificado em um computador local ou remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>Essa enumeração identifica Plug and Play tipos de eventos de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>Esta é uma estrutura de dados de evento de notificação de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>Estrutura do filtro de notificação do dispositivo<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td>A função <strong>CM_Open_Class_Key</strong> abre a chave do registro da classe de instalação do dispositivo, a chave do registro da classe da interface do dispositivo ou uma subchave específica de uma classe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td>A função <strong>CM_Open_Device_Interface_Key</strong> abre a subchave do registro que é usada por aplicativos e drivers para armazenar informações específicas a uma interface de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> A função <strong>CM_Open_Device_Interface_Key_ExA</strong> abre a subchave do registro que é usada por aplicativos e drivers para armazenar informações específicas a uma interface de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> A função <strong>CM_Open_Device_Interface_Key_ExW</strong> abre a subchave do registro que é usada por aplicativos e drivers para armazenar informações específicas a uma interface de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td>A função <strong>CM_Open_DevNode_Key</strong> abre uma chave do registro para obter informações de configuração específicas do dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td>A função <strong>CM_Query_And_Remove_SubTree</strong> verifica se uma instância de dispositivo e seus filhos podem ser removidos e, nesse caso, remove-os.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> .
</blockquote>
<br/> A função <strong>CM_Query_And_Remove_SubTree_Ex</strong> verifica se uma instância de dispositivo e seus filhos podem ser removidos e, nesse caso, remove-os.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td>A função <strong>CM_Query_Resource_Conflict_List</strong> identifica as instâncias de dispositivo que têm requisitos de recursos que entram em conflito com uma descrição de recurso da instância de dispositivo especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td>A função <strong>CM_Reenumerate_DevNode</strong> enumera os dispositivos identificados por um nó de dispositivo especificado e todos os seus filhos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> .
</blockquote>
<br/> A função <strong>CM_Reenumerate_DevNode_Ex</strong> enumera os dispositivos identificados por um nó de dispositivo especificado e todos os seus filhos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>Use <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification</strong></a> em vez de <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> se seu código tiver como alvo o Windows 7 ou versões anteriores do Windows. Os chamadores de modo kernel devem usar <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> em vez disso.<br/> A função <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> registra uma rotina de retorno de chamada de aplicativo a ser chamada quando ocorre um evento PnP do tipo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>A função <strong>CM_Request_Device_Eject</strong> prepara uma instância de dispositivo local para remoção segura, se o dispositivo for removível. Se o dispositivo puder ser ejetado fisicamente, será.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> .
</blockquote>
<br/> A função <strong>CM_Request_Device_Eject_Ex</strong> prepara uma instância de dispositivo local ou remota para remoção segura, se o dispositivo for removível. Se o dispositivo puder ser ejetado fisicamente, será.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td>A função <strong>CM_Request_Eject_PC</strong> solicita que um PC portátil, que é inserido em uma <a href="/windows-hardware/drivers/">estação de encaixe</a>local, seja ejetado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> .
</blockquote>
<br/> A função <strong>CM_Request_Eject_PC_Ex</strong> solicita que um PC portátil, que é inserido em uma <a href="/windows-hardware/drivers/">estação de encaixe</a>local ou remota, seja ejetado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td>A função <strong>CM_Set_Class_Property</strong> define uma propriedade de classe para uma classe de instalação de dispositivo ou uma classe de interface de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> .
</blockquote>
<br/> A função <strong>CM_Set_Class_Property_ExW</strong> define uma propriedade de classe para uma classe de instalação de dispositivo ou uma classe de interface de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td>A função <strong>CM_Set_Class_Registry_Property</strong> define ou exclui uma propriedade de uma <a href="/windows-hardware/drivers/install/device-setup-classes">classe de instalação de dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td>A função <strong>CM_Set_Device_Interface_Property</strong> define uma propriedade de dispositivo de uma interface de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> .
</blockquote>
<br/> A função <strong>CM_Set_Device_Interface_Property_ExW</strong> define uma propriedade de dispositivo de uma interface de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td>A função <strong>CM_Set_DevNode_Problem</strong> define um código de problema para um dispositivo que está instalado em um computador local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> .
</blockquote>
<br/> A função <strong>CM_Set_DevNode_Problem_Ex</strong> define um código de problema para um dispositivo que está instalado em um computador local ou remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td>A função <strong>CM_Set_DevNode_Property</strong> define uma propriedade de instância de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir do Windows 8 e do Windows Server 2012, essa função foi preterida. Em vez disso, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> .
</blockquote>
<br/> A função <strong>CM_Set_DevNode_Property_ExW</strong> define uma propriedade de instância de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td>A função <strong>CM_Set_DevNode_Registry_Property</strong> define uma propriedade de dispositivo especificada no registro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td>A função <strong>CM_Setup_DevNode</strong> reinicia uma instância de dispositivo que não está em execução porque há um problema com a configuração do dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td>A função <strong>CM_Uninstall_DevNode</strong> remove todo o estado persistente associado a uma instância de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>Use <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification</strong></a> em vez de <strong>CM_Unregister_Notification</strong> se seu código tiver como alvo o Windows 7 ou versões anteriores do Windows.<br/> A função <strong>CM_Unregister_Notification</strong> fecha o identificador HCMNOTIFICATION especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td>A função <strong>CMP_WaitNoPendingInstallEvents</strong> aguarda até que não haja nenhuma atividade pendente de instalação do dispositivo para o Gerenciador de PNP executar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>A estrutura de CONFLICT_DETAILS é usada como um parâmetro para a função <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>A estrutura de CS_DES é usada para especificar uma lista de recursos que descreve o uso de recursos específicos de classe de dispositivo para uma instância de dispositivo. Para obter mais informações sobre listas de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>A estrutura de CS_RESOURCE é usada para especificar uma lista de recursos que descreve o uso de recursos específicos de classe de dispositivo para uma instância de dispositivo. Para obter mais informações sobre listas de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>A estrutura de DMA_DES é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de canal DMA (acesso direto à memória) para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>A estrutura de DMA_RANGE especifica uma lista de requisitos de recursos que descreve o uso do canal de DMA para uma instância de dispositivo. Para obter mais informações sobre as listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>A estrutura de DMA_RESOURCE é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso do canal de DMA para uma instância de dispositivo. Para obter mais informações sobre lista de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>A estrutura de IO_DES é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de porta de e/s para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>A estrutura de IO_RANGE especifica uma lista de requisitos de recursos que descreve o uso de porta de e/s para uma instância de dispositivo. Para obter mais informações sobre as listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>A estrutura de IO_RESOURCE é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de porta de e/s para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>A estrutura de IRQ_DES é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de linha de IRQ para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>A estrutura de IRQ_RANGE especifica uma lista de requisitos de recursos que descreve o uso de linha de IRQ para uma instância de dispositivo. Para obter mais informações sobre as listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>A estrutura de IRQ_RESOURCE é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de linha de IRQ para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>A estrutura de MEM_DES é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de memória para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>A estrutura de MEM_RANGE especifica uma lista de requisitos de recursos que descreve o uso de memória para uma instância de dispositivo. Para obter mais informações sobre as listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>A estrutura de MEM_RESOURCE é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de memória para uma instância de dispositivo. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>A estrutura de MFCARD_DES é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de recursos por <em>uma</em> das funções de hardware fornecidas por uma instância de um dispositivo multifuncional. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>A estrutura de MFCARD_RESOURCE é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de recursos por <em>uma</em> das funções de hardware fornecidas por uma instância de um dispositivo multifuncional. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>A estrutura PCCARD_DES é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de recursos por uma instância de placa de PC. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>A estrutura PCCARD_RESOURCE é usada para especificar uma lista de recursos ou uma lista de requisitos de recursos que descreve o uso de recursos por uma instância de placa de PC. Para obter mais informações sobre listas de recursos e listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 

[Enviar comentários sobre este tópico para a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Enviar comentários sobre este tópico para a Microsoft")