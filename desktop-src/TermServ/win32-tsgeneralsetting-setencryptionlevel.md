---
title: Método SetEncryptionLevel da classe Win32_TSGeneralSetting
description: O método SetEncryptionLevel define o nível de criptografia.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetEncryptionLevel
- Método SetEncryptionLevel Serviços de Área de Trabalho Remota, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Serviços de Área de Trabalho Remota, método SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085861"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Método SetEncryptionLevel da classe Win32 \_ TSGeneralSetting

O método **SetEncryptionLevel** define o nível de criptografia.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MinEncryptionLevel* \[ no\]
</dt> <dd>

O nível de criptografia mínimo a ser definido.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Nível baixo de criptografia. Somente os dados enviados do cliente para o servidor são criptografados usando a criptografia de 56 bits. Observe que os dados enviados do servidor para o cliente não são criptografados.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Nível de criptografia compatível com o cliente. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados na força de chave máxima com suporte do cliente.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

Alto nível de criptografia. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados usando criptografia de 128 bits de alta segurança. Os clientes que não dão suporte a esse nível de criptografia não podem se conectar.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**quatro**


</dt> <dd>

Criptografia em conformidade com FIPS. Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados e descriptografados com os algoritmos de criptografia do padrão FIPS (FIPS) usando os módulos criptográficos da Microsoft. O FIPS é um padrão intitulado "requisitos de segurança para módulos criptográficos". O FIPS 140-1 (1994) e o FIPS 140-2 (2001) descrevem os requisitos governamentais dos módulos de criptografia de hardware e software usados no governo dos EUA.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGeneralSetting Win32**](win32-tsgeneralsetting.md)
</dt> </dl>

 

