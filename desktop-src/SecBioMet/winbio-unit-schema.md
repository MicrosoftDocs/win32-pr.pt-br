---
title: Estrutura de WINBIO_UNIT_SCHEMA (WinBio \_ Types. h)
description: Descreve os recursos de uma unidade biométrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_UNIT_SCHEMA
- ponteiro de estrutura de PWINBIO_UNIT_SCHEMA Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae91ae5353aa0e9c02414e90a8364d86bdc56c0cdcc4f4586656f28f92f100ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909165"
---
# <a name="winbio_unit_schema-structure"></a>Estrutura de esquema de \_ unidade WINBIO \_

A estrutura de **\_ \_ esquema de unidade WINBIO** descreve os recursos de uma unidade biométrica. Ele é usado pela função [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Unidadeid**
</dt> <dd>

Um valor que identifica a unidade biométrica.

</dd> <dt>

**Pooltype**
</dt> <dd>

Um valor **ULONG** que especifica o tipo da unidade biométrica. Esse valor pode ser um dos seguintes:



| Valor                                                                                                                                                                            | Significado                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_pool WINBIO \_ desconhecido**</dt> </dl> | O tipo é desconhecido.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_sistema de pool WINBIO \_**</dt> </dl>    | A sessão se conecta a uma coleção compartilhada de unidades biométricas gerenciadas pelo provedor de serviços.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**WINBIO \_ pool \_ privado**</dt> </dl> | A sessão se conecta a uma coleção de unidades biométricas que são gerenciadas pelo chamador.<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

Um valor que especifica o tipo da unidade biométrica. No momento, somente a **\_ \_ impressão digital do tipo WINBIO** é suportada.

</dd> <dt>

**SensorSubType**
</dt> <dd>

Um subtipo de sensor definido para o tipo biométrico especificado pelo membro **BiometricFactor** . Atualmente, há suporte apenas para tipos de impressão digital (**\_ \_ impressão digital do tipo WINBIO**). Os seguintes subtipos estão atualmente definidos para impressões digitais:

-   subtipo de \_ sensor WINBIO \_ \_ desconhecido
-   \_deslize o \_ \_ subtipo do \_ sensor de WINBIO FP
-   \_toque de \_ \_ subtipo de \_ sensor de WINBIO FP

</dd> <dt>

**Funcionalidades**
</dt> <dd>

Um bitmask dos recursos do sensor biométrico. Isso pode ser um valor de bits **ou** um dos seguintes valores:

-   \_sensor de capacidade de WINBIO \_
-   \_correspondência de capacidade de WINBIO \_
-   banco de dados de \_ funcionalidades WINBIO \_
-   \_processamento de recursos WINBIO \_
-   \_criptografia de recurso WINBIO \_
-   \_navegação de capacidade do WINBIO \_
-   \_indicador de funcionalidade de WINBIO \_
-   \_ \_ sensor virtual de funcionalidade de WINBIO \_
    > [!Note]  
    > a constante do **\_ \_ \_ SENSOR VIRTUAL de funcionalidade do WINBIO** aplica-se somente ao Windows 10 e posterior.

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

Um valor de cadeia de caracteres que contém a ID do dispositivo. A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.

</dd> <dt>

**Descrição**
</dt> <dd>

Um valor de cadeia de caracteres que contém uma descrição da unidade biométrica. A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.

</dd> <dt>

**Manufacturer**
</dt> <dd>

Um valor de cadeia de caracteres que contém o nome do fabricante. A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.

</dd> <dt>

**Modelo**
</dt> <dd>

Um valor de cadeia de caracteres que contém o número do modelo da unidade biométrica. A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.

</dd> <dt>

**SerialNumber**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em **nulo** que contém o número de série da unidade biométrica. A cadeia de caracteres pode conter até 256 caracteres Unicode, incluindo um caractere **nulo** de terminação.

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

Uma estrutura de [**\_ versão do WINBIO**](winbio-version.md) que contém os números de versão principal e secundária para a unidade biométrica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





