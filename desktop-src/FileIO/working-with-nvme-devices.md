---
description: Saiba como trabalhar com dispositivos NVMe de alta velocidade de seu aplicativo do Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Trabalhando com unidades NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766911"
---
# <a name="working-with-nvme-drives"></a>Trabalhando com unidades NVMe

**Aplica-se a:**

-   Windows 10
-   Windows Server 2016

Saiba como trabalhar com dispositivos NVMe de alta velocidade de seu aplicativo do Windows. O acesso ao dispositivo é habilitado via **StorNVMe.sys**, o driver na caixa introduzido primeiro no Windows Server 2012 R2 e no Windows 8.1. Ele também está disponível para dispositivos Windows 7 por meio de um Hot Fix do KB. No Windows 10, vários novos recursos foram introduzidos, incluindo um mecanismo de passagem para comandos do NVMe específicos do fornecedor e atualizações para os IOCTLs existentes.

Este tópico fornece uma visão geral das APIs de uso geral que você pode usar para acessar as unidades do NVMe no Windows 10. Ele também descreve:

-   Como enviar um comando do NVMe específico do fornecedor com [passagem](#pass-through-mechanism)
-   Como [enviar um comando de identificação, obter recursos ou obter páginas de log](#protocol-specific-queries) para a unidade NVMe
-   Como [obter informações de temperatura](#temperature-queries) de uma unidade NVMe
-   Como executar comandos de alteração de comportamento, como a [configuração de limites de temperatura](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>APIs para trabalhar com unidades NVMe

Você pode usar as seguintes APIs de uso geral para acessar as unidades do NVMe no Windows 10. Essas APIs podem ser encontradas em **winioctl. h** para aplicativos de modo de usuário e **ntddstor. h** para drivers de modo kernel. Para obter mais informações sobre arquivos de cabeçalho, consulte [arquivos de cabeçalho](#header-files).

-   [**IOCTL \_ \_ \_ Comando de protocolo de armazenamento**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use este IOCTL com a estrutura de **\_ \_ comando do protocolo de armazenamento** para emitir comandos do NVMe. Esse IOCTL habilita a passagem de NVMe e dá suporte ao log de efeitos de comando no NVMe. Você pode usá-lo com comandos específicos do fornecedor. Para obter mais informações, consulte [mecanismo de passagem](#pass-through-mechanism).

-   [**Armazenamento \_ do \_Comando de protocolo**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : essa estrutura de buffer de entrada inclui um campo **ReturnStatus** que pode ser usado para relatar os valores de status a seguir.
    -   **STATUS do protocolo de armazenamento \_ \_ \_ pendente**
    -   **\_êxito do \_ status do protocolo de armazenamento \_**
    -   **\_erro de \_ status do protocolo de armazenamento \_**
    -   **\_ \_ \_ solicitação inválida de status do protocolo de armazenamento \_**
    -   **STATUS do protocolo de armazenamento \_ \_ \_ sem \_ dispositivo**
    -   **STATUS de protocolo de armazenamento \_ \_ \_ ocupado**
    -   **\_saturação de \_ dados de status do protocolo de armazenamento \_ \_**
    -   **\_ \_ \_ recursos insuficientes do status do protocolo de armazenamento \_**
    -   **STATUS do protocolo de armazenamento \_ \_ \_ não \_ suportado**
-   [**IOCTL \_ \_ \_ Propriedade de consulta de armazenamento**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use este IOCTL com a estrutura de **\_ \_ consulta de propriedade de armazenamento** para recuperar informações do dispositivo. Para obter mais informações, consulte [consultas específicas de protocolo](#protocol-specific-queries) e [consultas de temperatura](#temperature-queries).

-   [**Armazenamento \_ do \_Consulta de propriedade**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : essa estrutura inclui os campos **PropertyId** e **AdditionalParameters** para especificar os dados a serem consultados. Na **PropertyId** arquivada, use a enumeração de **\_ \_ ID de propriedade de armazenamento** para especificar o tipo de dados. Use o campo **AdditionalParameters** para especificar mais detalhes, dependendo do tipo de dados. Para dados específicos de protocolo, use a estrutura de **\_ \_ \_ dados específica do protocolo de armazenamento** no campo **AdditionalParameters** . Para dados de temperatura, use a estrutura **\_ \_ informações de temperatura de armazenamento** no campo **AdditionalParameters** .
-   [**Armazenamento \_ do \_ID da propriedade**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : essa enumeração inclui novos valores que permitem que a **\_ \_ \_ propriedade de consulta de armazenamento do IOCTL** recupere informações específicas de protocolo e de temperatura.

    -   **StorageAdapterProtocolSpecificProperty**
    -   **StorageDeviceProtocolSpecificProperty**

    Use uma dessas IDs de propriedade específicas de protocolo em combinação com **\_ \_ \_ dados específicos do protocolo de armazenamento** para recuperar dados específicos do protocolo na estrutura do [**\_ \_ \_ descritor de dados do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    Use uma dessas IDs de propriedade de temperatura para recuperar dados de temperatura na estrutura do [**\_ \_ \_ descritor de dados de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .

-   [**Armazenamento \_ do \_ \_ Dados específicos do protocolo**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : recupere dados específicos do NVMe quando essa estrutura é usada para o campo **AdditionalParameters** da **\_ \_ consulta de propriedade de armazenamento** e um valor de enumeração de [**\_ \_ \_ \_ tipo de dados de protocolo de armazenamento NVMe**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) é especificado. Use um dos seguintes valores **de \_ \_ tipo de \_ dados \_ NVME do protocolo de armazenamento** no campo **DataType** da estrutura de **\_ \_ \_ dados específica do protocolo de armazenamento** :

    -   Use **NVMeDataTypeIdentify** para obter dados do controlador de identificação ou identificar dados de namespace.
    -   Use **NVMeDataTypeLogPage** para obter páginas de log (incluindo dados inteligentes/de integridade).
    -   Use **NVMeDataTypeFeature** para obter recursos da unidade NVMe.

-   [**Armazenamento \_ do \_Informações de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : essa estrutura é usada para manter dados de temperatura específicos. Ele é usado no **\_ \_ \_ descritor de dados TEMERATURE de armazenamento** para retornar os resultados de uma consulta de temperatura.

-   [**IOCTL \_ \_Limite de \_ temperatura \_ do conjunto de armazenamento**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use este IOCTL com a estrutura de **\_ \_ limite de temperatura de armazenamento** para definir limites de temperatura. Para obter mais informações, consulte [comportamento alterando comandos](#behavior-changing-commands).

-   [**Armazenamento \_ do \_Limite de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : essa estrutura é usada como um buffer de entrada para especificar o limite de temperatura. O campo de **limite** excedente (booliano) especifica se o campo de **limite** é acima do valor limite ou não (caso contrário, é o valor de limite).

## <a name="pass-through-mechanism"></a>Mecanismo de passagem

Os comandos que não são definidos na especificação NVMe são os mais difíceis para o sistema operacional host lidar – o host não tem informações sobre os efeitos que os comandos podem ter no dispositivo de destino, a infraestrutura exposta (namespaces/tamanhos de bloco) e seu comportamento.

Para executar melhor esses comandos específicos do dispositivo por meio da pilha de armazenamento do Windows, um novo mecanismo de passagem permite que comandos específicos do fornecedor sejam canalizados. Esse pipe de passagem também ajudará no desenvolvimento de ferramentas de gerenciamento e teste. No entanto, esse mecanismo de passagem requer o uso do log de efeitos de comando. Além disso, StoreNVMe.sys exige que todos os comandos, não apenas os comandos de passagem, sejam descritos no log de efeitos de comando.

> [!IMPORTANT]
> StorNVMe.sys e Storport.sys bloquearão qualquer comando para um dispositivo se ele não estiver descrito no log de efeitos de comando.

 

### <a name="supporting-the-command-effects-log"></a>Suporte ao log de efeitos de comando

O log de efeitos de comando (conforme descrito em comandos com suporte e efeitos, a seção 5.10.1.5 da [especificação do NVMe 1,2](https://nvmexpress.org/specifications)) permite a descrição dos efeitos de comandos específicos do fornecedor em conjunto com comandos definidos pela especificação. Isso facilita a validação de suporte de comandos, bem como a otimização do comportamento do comando, e, portanto, deve ser implementado para todo o conjunto de comandos que o dispositivo suporta. As condições a seguir descrevem o resultado de como o comando é enviado com base em sua entrada de log de efeitos de comando.

Para qualquer comando específico descrito no log de efeitos de comando...

**Embora**:

-   O comando com suporte (CSUPP) está definido como ' 1 ', indicando que o comando tem suporte do controlador (bit 01)

    > [!Note]  
    > Quando CSUPP é definido como ' 0 ' (indicando que não há suporte para o comando), o comando será bloqueado

     

**E se** qualquer um dos seguintes for definido:

-   A alteração de capacidade do controlador (CCC) está definida como ' 1 ', indicando que o comando pode alterar os recursos do controlador (bit 04)

-   A NIC (alteração de inventário) de namespace está definida como ' 1 ', indicando que o comando pode alterar o número ou recursos para vários namespaces (bit 03)

-   A NCC (alteração de capacidade de namespace) está definida como ' 1 ', indicando que o comando pode alterar os recursos de um único namespace (bit 02)

-   A CSE (envio e execução de comando) é definida como 001B ou 010b, significando que o comando pode ser enviado quando não há nenhum outro comando pendente para o mesmo ou qualquer namespace, e esse outro comando não deve ser enviado para o mesmo ou para qualquer namespace até que esse comando seja concluído (bits 18:16)

**Em seguida,** o comando será enviado como o único comando pendente para o adaptador.

**Caso contrário, se**:

-   A CSE (envio e execução de comando) é definida como 001B, indicando que o comando pode ser enviado quando não há nenhum outro comando pendente para o mesmo namespace e que outro comando não deve ser enviado ao mesmo namespace até que esse comando seja concluído (bits 18:16)

**Em seguida,** o comando será enviado como o único comando pendente para o objeto de número de unidade lógica (LUN).

**Caso contrário**, o comando é enviado com outros comandos pendentes sem inibição. Por exemplo, se um comando específico do fornecedor for enviado para o dispositivo para recuperar informações estatísticas que não são definidas pela especificação, não deverá haver nenhum risco para alterar o comportamento do dispositivo ou a capacidade de executar comandos de e/s. Essas solicitações podem ser atendidas em paralelo à e/s e nenhum Pause-retomar será necessário.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Usando o \_ \_ comando de protocolo de armazenamento do IOCTL \_ para enviar comandos

A passagem pode ser realizada usando o [**comando de \_ \_ protocolo de \_ armazenamento do IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduzido no Windows 10. Esse IOCTL foi projetado para ter um comportamento semelhante como os IOCTLs de passagem SCSI e ATA existentes, para enviar um comando incorporado ao dispositivo de destino. Por meio desse IOCTL, a passagem pode ser enviada para um dispositivo de armazenamento, incluindo uma unidade NVMe.

Por exemplo, no NVMe, o IOCTL permitirá o envio dos seguintes códigos de comando.

-   Comandos de administrador específicos do fornecedor (C0h – FFh)
-   Comandos de NVMe específicos do fornecedor (80h – FFh)

Assim como acontece com todos os outros IOCTLs, use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar o IOCTL de passagem para baixo. O IOCTL é populado usando a estrutura de buffer de entrada do [**\_ \_ comando do protocolo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) encontrada em **ntddstor. h**. Preencha o campo de **comando** com o comando específico do fornecedor.


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



O comando específico do fornecedor desejado para ser enviado deve ser preenchido no campo realçado acima. Observe novamente que o log de efeitos de comando deve ser implementado para comandos de passagem. Em particular, esses comandos precisam ser relatados como com suporte no log de efeitos de comando (consulte a seção anterior para obter mais informações). Observe também que os campos da PRP são específicos do driver, portanto, os aplicativos que enviam comandos podem deixá-los como 0.

Por fim, esse IOCTL de passagem destina-se ao envio de comandos específicos do fornecedor. Para enviar outros comandos do NVMe ou não específicos do fornecedor, como identificar, esse IOCTL de passagem não deve ser usado. Por exemplo, **a \_ \_ \_ propriedade de consulta de armazenamento de IOCTL** deve ser usada para identificar ou obter páginas de log. Para obter mais informações, consulte a próxima seção, [consultas específicas de protocolo](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>Não atualizar o firmware por meio do mecanismo de passagem

Os comandos de download e ativação de firmware não devem ser enviados usando passagem. **IOCTL \_ O \_ \_ comando de protocolo de armazenamento** só deve ser usado para comandos específicos do fornecedor.

Em vez disso, use os seguintes IOCTLs de armazenamento geral (introduzidos no Windows 10) para evitar aplicativos diretamente usando a \_ versão de miniporta SCSI do firmware IOCTL. Os drivers de armazenamento irão converter o IOCTL em um comando SCSI ou na \_ versão de miniporta SCSI do IOCTL para a miniporta.

Esses IOCTLs são recomendados para o desenvolvimento de ferramentas de atualização de firmware no Windows 10 e no Windows Server 2016:

-   [**\_informações de \_ obtenção do firmware de armazenamento do IOCTL \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**\_download do \_ firmware de armazenamento do IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**\_ativação do \_ firmware de armazenamento do IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Para obter informações de armazenamento e atualizar o firmware, o Windows também dá suporte a cmdlets do PowerShell para fazer isso rapidamente:

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Para atualizar o firmware no NVMe no Windows 8.1, use \_ o \_ firmware de miniporta SCSI do IOCTL \_ . Este IOCTL não foi reportado para o Windows 7. Para obter mais informações, consulte [atualizando o firmware para um dispositivo NVMe no Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Retornando erros por meio do mecanismo de passagem

Semelhante aos IOCTLs de passagem SCSI e ATA, quando um comando/solicitação é enviado para a miniporta ou dispositivo, o IOCTL retorna se ele foi bem-sucedido ou não. Na estrutura [**de \_ \_ comando do protocolo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , o IOCTL retorna o status por meio do campo **ReturnStatus** .

### <a name="example-sending-a-vendor-specific-command"></a>Exemplo: enviando um comando específico do fornecedor

Neste exemplo, um comando arbitrário específico do fornecedor (0xFF) é enviado por passagem para uma unidade NVMe. O código a seguir aloca um buffer, Inicializa uma consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



Neste exemplo, esperamos que `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` o comando tenha sido bem-sucedido para o dispositivo.

## <a name="protocol-specific-queries"></a>Consultas específicas de protocolo

Windows 8.1 introduziu a propriedade de consulta de armazenamento de IOCTL para recuperação de dados. [**\_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) No Windows 10, o IOCTL foi aprimorado para dar suporte a recursos de NVMe comumente solicitados, como **obter páginas de log**, **obter recursos** e **identificar**. Isso permite a recuperação de informações específicas de NVMe para fins de monitoramento e inventário.

O buffer de entrada para o IOCTL [**, \_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (do Windows 10) é mostrado aqui.


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Ao usar [**a \_ \_ \_ propriedade de consulta de armazenamento do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para recuperar informações específicas do protocolo NVMe no [**\_ \_ \_ descritor de dados do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure a estrutura de [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) da seguinte maneira:

-   Aloque um buffer que possa conter uma [**consulta de \_ propriedade \_ de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) e uma estrutura de [**\_ \_ \_ dados específica de protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .

-   Defina o campo **PropertyId** como **StorageAdapterProtocolSpecificProperty** ou **StorageDeviceProtocolSpecificProperty** para uma solicitação de controlador ou dispositivo/namespace, respectivamente.

-   Defina o campo **QueryType** como **PropertyStandardQuery**.

-   Preencha a estrutura de [**\_ \_ \_ dados específica do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) com os valores desejados. O início dos **\_ \_ \_ dados específicos do protocolo de armazenamento** é o campo **adicionalparameters** da [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

A estrutura de [**\_ \_ \_ dados específica do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (do Windows 10) é mostrada aqui.


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



Para especificar um tipo de informações específicas do protocolo NVMe, configure a estrutura de [**\_ \_ \_ dados específica do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) da seguinte maneira:

-   Defina o campo **ProtocolType** como **ProtocolTypeNVMe**.

-   Defina o campo **DataType** como um valor de enumeração definido [**pelo \_ \_ tipo de \_ dados \_ NVME do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):

    -   Use **NVMeDataTypeIdentify** para obter dados do controlador de identificação ou identificar dados de namespace.
    -   Use **NVMeDataTypeLogPage** para obter páginas de log (incluindo dados inteligentes/de integridade).
    -   Use **NVMeDataTypeFeature** para obter recursos da unidade NVMe.

Quando **ProtocolTypeNVMe** é usado como o **ProtocolType**, as consultas para informações específicas de protocolo podem ser recuperadas em paralelo com outras e/s na unidade NVMe.

Os exemplos a seguir demonstram consultas específicas do protocolo NVMe.

### <a name="example-nvme-identify-query"></a>Exemplo: NVMe identificar consulta

Neste exemplo, a solicitação **identificar** é enviada para uma unidade NVMe. O código a seguir inicializa a estrutura de dados de consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



Observe que o chamador precisa alocar um único buffer contendo \_ a consulta de propriedade de armazenamento \_ e o tamanho dos \_ dados específicos do protocolo de armazenamento \_ \_ . Neste exemplo, ele está usando o mesmo buffer para entrada e saída da consulta de propriedade. É por isso que o buffer que foi alocado tem um tamanho de " \_ deslocamento de campo \_ ( \_ consulta de propriedade de armazenamento, adicionalparameters) + sizeof ( \_ dados específicos de protocolo de armazenamento \_ \_ ) + \_ tamanho máximo de log de NVME \_ \_ ". Embora buffers separados pudessem ser alocados para entrada e saída, é recomendável usar um único buffer para consultar informações relacionadas ao NVMe.

### <a name="example-nvme-get-log-pages-query"></a>Exemplo: NVMe obter consulta de páginas de log

Neste exemplo, com base no anterior, a solicitação _ *obter páginas do log** é enviada para uma unidade NVMe. O código a seguir prepara a estrutura de dados de consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Exemplo: consulta de obter recursos do NVMe

Neste exemplo, com base no anterior, a solicitação _ *Get Features** é enviada para uma unidade NVMe. O código a seguir prepara a estrutura de dados de consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a>Conjunto específico de protocolo

No Windows 10 19H1, o IOCTL_STORAGE_SET_PROPERTY foi aprimorado para oferecer suporte a recursos do NVMe set.

O buffer de entrada para o IOCTL_STORAGE_SET_PROPERTY é mostrado aqui:

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

Ao usar IOCTL_STORAGE_SET_PROPERTY para definir o recurso NVMe, configure a estrutura de STORAGE_PROPERTY_SET da seguinte maneira:

-   Alocar um buffer que pode conter um STORAGE_PROPERTY_SET e uma estrutura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
-   Defina o campo PropertyId como StorageAdapterProtocolSpecificProperty ou StorageDeviceProtocolSpecificProperty para uma solicitação de controlador ou dispositivo/namespace, respectivamente.
-   Preencha a estrutura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT com os valores desejados. O início da STORAGE_PROTOCOL_SPECIFIC_DATA_EXT é o campoparameters adicional de STORAGE_PROPERTY_SET.

A estrutura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT é mostrada aqui.

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

Para especificar um tipo de recurso NVMe a ser definido, configure a estrutura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT da seguinte maneira:
-   Defina o campo ProtocolType como ProtocolTypeNvme;
-   Defina o campo DataType para o valor de enumeração NVMeDataTypeFeature definido por STORAGE_PROTOCOL_NVME_DATA_TYPE;

Os exemplos a seguir demonstram o conjunto de recursos do NVMe.

### <a name="example-nvme-set-features"></a>Exemplo: NVMe Set Features

Neste exemplo, a solicitação definir recursos é enviada para uma unidade NVMe. O código a seguir prepara a estrutura de dados definida e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a>Consultas de temperatura

No Windows 10, [**a \_ \_ \_ propriedade de consulta de armazenamento do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) também pode ser usada para consultar dados de temperatura de dispositivos NVMe.

Para recuperar informações de temperatura de uma unidade NVMe no [**\_ \_ \_ descritor de dados de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure a estrutura de [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) da seguinte maneira:

-   Aloque um buffer que possa conter uma estrutura de [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .

-   Defina o campo **PropertyId** como **StorageAdapterTemperatureProperty** ou **StorageDeviceTemperatureProperty** para uma solicitação de controlador ou dispositivo/namespace, respectivamente.

-   Defina o campo **QueryType** como **PropertyStandardQuery**.

A estrutura de [**\_ \_ informações de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (do Windows 10) é mostrada aqui.


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a>Comandos de alteração de comportamento

Comandos que manipulam atributos de dispositivo ou potencialmente impactam o comportamento do dispositivo são mais difíceis de lidar com o sistema operacional. Se os atributos do dispositivo forem alterados em tempo de execução enquanto a e/s estiver sendo processada, poderão ocorrer problemas de integridade de dados ou de sincronização se não forem manipulados corretamente.

O comando NVMe **set-Features** é um bom exemplo de um comando de alteração de comportamento. Ele permite a alteração do mecanismo de arbitragem e a configuração de limites de temperatura. Para garantir que os dados em trânsito não estejam em risco quando os comandos set que afetam o comportamento forem enviados, o Windows pausará todas as e/s no dispositivo NVMe, as filas de drenagem e os buffers de liberação. Depois que o comando Set for executado com êxito, a e/s será retomada (se possível). Se a e/s não puder ser retomada, uma redefinição de dispositivo poderá ser necessária.

### <a name="setting-temperature-thresholds"></a>Definindo limites de temperatura

O Windows 10 introduziu o limite de temperatura do conjunto de armazenamento do IOCTL, um IOCTL para obter e definir limites de temperatura. [**\_ \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) Você também pode usá-lo para obter a temperatura atual do dispositivo. O buffer de entrada/saída para este IOCTL é a estrutura de [**\_ \_ informações de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , da seção de código anterior.

### <a name="example-setting-over-threshold-temperature"></a>Exemplo: definindo a temperatura excedente do limite

Neste exemplo, a temperatura excedente do limite de uma unidade de NVMe está definida. O código a seguir prepara o comando e, em seguida, o envia para o dispositivo por meio de DeviceIoControl.


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a>Configurando recursos específicos do fornecedor

Sem o log de efeitos de comando, o driver não tem conhecimento das ramificações do comando. É por isso que o log de efeitos de comando é necessário. Ele ajuda o sistema operacional a determinar se um comando tem um impacto alto e se ele pode ser enviado em paralelo com outros comandos para a unidade.

O log de efeitos de comando ainda não é granular o suficiente para abranger os comandos **set-Features** específicos do fornecedor. Por esse motivo, ainda não é possível enviar comandos **set-Features** específicos do fornecedor. No entanto, é possível usar o mecanismo de passagem, discutido anteriormente, para enviar comandos específicos do fornecedor. Para obter mais informações, consulte [mecanismo de passagem](#pass-through-mechanism).

## <a name="header-files"></a>Arquivos de cabeçalho

Os arquivos a seguir são relevantes para o desenvolvimento do NVMe. Esses arquivos estão incluídos no [SDK (Software Development Kit) do Microsoft Windows](https://developer.microsoft.com/windows/downloads).



| Arquivo de cabeçalho    | Descrição                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor. h** | Define constantes e tipos para acessar os drivers de classe de armazenamento do modo kernel.   |
| **nvme. h**     | Para outras estruturas de dados relacionadas ao NVMe.                                                 |
| **winioctl. h** | Para definições gerais de IOCTL do Win32, incluindo APIs de armazenamento para aplicativos de modo de usuário. |



 

 

 
