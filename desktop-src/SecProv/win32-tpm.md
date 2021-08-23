---
description: Representa o Trusted Platform Module (TPM), um chip de segurança de hardware que fornece uma raiz de confiança para um sistema de computador.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Win32_Tpm classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 53fbe055e469dc4327ae747ab3e20873724923980f1e765d266a5f8143b545c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004014"
---
# <a name="win32_tpm-class"></a>Classe Win32 \_ Tpm

A **classe \_ Win32 Tpm** representa o Trusted Platform Module (TPM), um chip de segurança de hardware que fornece uma raiz de confiança para um sistema de computador.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a>Membros

A **classe \_ Win32 Tpm** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Win32 Tpm** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBlockedCommand**](addblockedcommand-win32-tpm.md)                                 | Adiciona um comando TPM à lista local de comandos bloqueados Windows.<br/>                                                                                                             |
| [**ChangeOwnerAuth**](changeownerauth-win32-tpm.md)                                     | Altera o valor de autorização do proprietário do TPM.<br/>                                                                                                                                       |
| [**Limpar**](clear-win32-tpm.md)                                                         | Redefine o TPM para seu estado padrão de fábrica.<br/>                                                                                                                                     |
| [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md)                               | Converte uma frase-senha fornecida pelo usuário em um valor de autorização de proprietário de 20 byte que pode ser usado para interagir com o TPM.<br/>                                                            |
| [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)                   | Cria um par de chaves de endosso de 2048 bits no TPM.<br/>                                                                                                                              |
| [**Desabilitar**](disable-win32-tpm.md)                                                     | Permite que o proprietário do TPM desabilite o TPM.<br/>                                                                                                                                         |
| [**Habilitar**](enable-win32-tpm.md)                                                       | Permite que o proprietário do TPM habilita o TPM.<br/>                                                                                                                                          |
| [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)               | Obtém e retorna a operação de presença física TPM pendente. Use o [**método SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.<br/> |
| [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)             | Obtém e retorna os resultados de uma operação de presença física do TPM que foi executada.<br/>                                                                                          |
| [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)         | Indica a ação do usuário necessária para executar uma operação de presença física do TPM.<br/>                                                                                           |
| [**Ativado**](isactivated-win32-tpm.md)                                             | Indica se o TPM está ativado.<br/>                                                                                                                                          |
| [**IsCommandBlocked**](iscommandblocked-win32-tpm.md)                                   | Indica se o comando TPM pode ser executado nesse sistema operacional.<br/>                                                                                                              |
| [**IsCommandPresent**](iscommandpresent-win32-tpm.md)                                   | Indica se há suporte para um comando TPM neste computador.<br/>                                                                                                                   |
| [**IsEnabled**](isenabled-win32-tpm.md)                                                 | Indica se o TPM está habilitado.<br/>                                                                                                                                            |
| [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md)             | Indica se o TPM tem um par de chaves de endosso.<br/>                                                                                                                           |
| [**IsOwned**](isowned-win32-tpm.md)                                                     | Indica se o TPM tem um proprietário.<br/>                                                                                                                                          |
| [**IsOwnerClearDisabled**](isownercleardisabled-win32-tpm.md)                           | Indica se o proprietário do TPM pode limpar o TPM.<br/>                                                                                                                               |
| [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)                               | Indica se um proprietário do TPM pode ser instalado.<br/>                                                                                                                                  |
| [**IsPhysicalClearDisabled**](isphysicalcleardisabled-win32-tpm.md)                     | Indica se uma operação de presença física do TPM pode limpar o TPM.<br/>                                                                                                           |
| [**IsPhysicalPresenceHardwareEnabled**](isphysicalpresencehardwareenabled-win32-tpm.md) | Indica se este computador dá suporte a um caminho de hardware dedicado para sinalizar a presença física.<br/>                                                                                  |
| [**IsSrkAuthCompatible**](issrkauthcompatible-win32-tpm.md)                             | Indica se a autorização Armazenamento SRK (chave raiz) é compatível com Windows.<br/>                                                                                           |
| [**RemoveBlockedCommand**](removeblockedcommand-win32-tpm.md)                           | Remove um comando TPM da lista local de comandos bloqueados por Windows.<br/>                                                                                                        |
| [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)                                   | Redefine o período de tempo-tempo ou outro mecanismo que os fabricantes do TPM implementam para proteger contra ataques de dicionário no TPM.<br/>                                                 |
| [**ResetSrkAuth**](resetsrkauth-win32-tpm.md)                                           | Redefine o valor Armazenamento de autorização da chave raiz (SRK) para ser compatível com Windows.<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | Executa um auto teste do TPM e retorna o resultado.<br/>                                                                                                                          |
| [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)               | Solicita uma operação de presença física do TPM para ser executado.<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | Instala um proprietário para o TPM.<br/>                                                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A **classe \_ Win32 Tpm** tem essas propriedades.

<dl> <dt>

**IsActivated \_ InitialValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o TPM está ativado.

**true** se o dispositivo estiver ativado (ou seja, se **IsActivated \_ InitialValue** for true); caso contrário, **false**.

Esse valor é armazenado quando a classe é instautada. É possível que o TPM altere o estado entre a insta instação e quando você verifica esse valor. Para verificar se o TPM está ativado em tempo real, use o [**método IsActivated.**](isactivated-win32-tpm.md)

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível.

</dd> <dt>

**IsEnabled \_ InitialValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o TPM está habilitado.

**true** se o dispositivo estiver habilitado (ou seja, se **IsEnabled \_ InitialValue** for true); caso contrário, **false**.

Esse valor é armazenado quando a classe é instautada. É possível que o TPM altere o estado entre a insta instação e quando você verifica esse valor. Para verificar se o TPM está habilitado em tempo real, use o [**método IsEnabled.**](isenabled-win32-tpm.md)

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível.

</dd> <dt>

**IsOwned \_ InitialValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o TPM tem um proprietário.

**true** se o dispositivo tiver um proprietário (ou seja, se **IsOwned \_ InitialValue** for true); caso contrário, **false.**

Esse valor é armazenado quando a classe é instautada. É possível que o TPM altere o estado entre a insta instação e quando você verifica esse valor. Para verificar se o TPM pertence em tempo real, use o [**método IsOwned.**](isowned-win32-tpm.md)

**Windows Server 2008 e Windows Vista:** Essa propriedade não está disponível.

</dd> <dt>

**ManufacturerId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As informações de identificação que nomeia exclusivamente o fabricante do TPM.

Quando os dados não estão disponíveis, zero é retornado.

Esse valor inteiro pode ser convertido em um valor de cadeia de caracteres interpretando cada byte como um caractere ASCII. Por exemplo, um valor inteiro de 1414548736 pode ser dividido nesses 4 bytes: 0x54, 0x50, 0x4D e 0x00. Supondo que a cadeia de caracteres seja interpretada da esquerda para a direita, esse valor inteiro é convertido em um valor de cadeia de caracteres de "TPM".

</dd> <dt>

**ManufacturerVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão do TPM, conforme especificado pelo fabricante.

Quando os dados não estão disponíveis, "Sem suporte" é retornado.

</dd> <dt>

**ManufacturerVersionInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Outras informações de versão específicas do fabricante para o TPM.

Quando os dados não estão disponíveis, "Sem suporte" é retornado.

</dd> <dt>

**PhysicalPresenceVersionInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão da Interface de Presença Física, um mecanismo de comunicação usado para executar operações de dispositivo que exigem presença física, compatível com o computador.

Essa interface deve estar disponível para executar operações de presença física do TPM. Os métodos **Win32 \_ Tpm** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)e [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expõem os recursos da Interface de Presença Física.

Quando os dados não estão disponíveis, "Sem suporte" é retornado.

</dd> <dt>

**SpecVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão da especificação Trusted Computing Group (TCG) compatível com o TPM. Esse valor inclui a versão da especificação de TCG principal e secundária, o nível de revisão da especificação e o nível de revisão errata. Todos os valores estão em hexadecimal. Por exemplo, uma informação de versão de "1.2, 2, 0" indica que o dispositivo foi implementado para a especificação TCG versão 1.2, nível de revisão 2 e sem errata.

Quando os dados não estão disponíveis, "Sem suporte" é retornado.

</dd> </dl>

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                      |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



 

 
