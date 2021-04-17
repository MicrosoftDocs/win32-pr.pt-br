---
description: Representa o Trusted Platform Module (TPM), um chip de segurança de hardware que fornece uma raiz de confiança para um sistema de computador.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Classe Win32_Tpm
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
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756146"
---
# <a name="win32_tpm-class"></a>\_Classe TPM do Win32

A classe **Win32 \_ TPM** representa o Trusted Platform Module (TPM), um chip de segurança de hardware que fornece uma raiz de confiança para um sistema de computador.

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

A classe **Win32 \_ TPM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TPM** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBlockedCommand**](addblockedcommand-win32-tpm.md)                                 | Adiciona um comando TPM à lista local de comandos bloqueados no Windows.<br/>                                                                                                             |
| [**ChangeOwnerAuth**](changeownerauth-win32-tpm.md)                                     | Altera o valor de autorização do proprietário do TPM.<br/>                                                                                                                                       |
| [**Formatação**](clear-win32-tpm.md)                                                         | Redefine o TPM para seu estado de fábrica-padrão.<br/>                                                                                                                                     |
| [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md)                               | Converte uma frase secreta fornecida pelo usuário em um valor de autorização de proprietário de 20 bytes que pode ser usado para interagir com o TPM.<br/>                                                            |
| [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)                   | Cria um par de chaves de endosso de 2048 bits no TPM.<br/>                                                                                                                              |
| [**Desabilitar**](disable-win32-tpm.md)                                                     | Permite que o proprietário do TPM desabilite o TPM.<br/>                                                                                                                                         |
| [**Habilitar**](enable-win32-tpm.md)                                                       | Permite que o proprietário do TPM habilite o TPM.<br/>                                                                                                                                          |
| [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)               | Obtém e retorna a operação de presença física de TPM pendente. Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.<br/> |
| [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)             | Obtém e retorna os resultados de uma operação de presença física de TPM que foi executada.<br/>                                                                                          |
| [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)         | Indica a ação do usuário necessária para executar uma operação de presença física do TPM.<br/>                                                                                           |
| [**Isactivad**](isactivated-win32-tpm.md)                                             | Indica se o TPM está ativado.<br/>                                                                                                                                          |
| [**IsCommandBlocked**](iscommandblocked-win32-tpm.md)                                   | Indica se o comando TPM pode ser executado neste sistema operacional.<br/>                                                                                                              |
| [**IsCommandPresent**](iscommandpresent-win32-tpm.md)                                   | Indica se há suporte para um comando TPM neste computador.<br/>                                                                                                                   |
| [**IsEnabled**](isenabled-win32-tpm.md)                                                 | Indica se o TPM está habilitado.<br/>                                                                                                                                            |
| [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md)             | Indica se o TPM tem um par de chaves de endosso.<br/>                                                                                                                           |
| [**Isdele**](isowned-win32-tpm.md)                                                     | Indica se o TPM tem um proprietário.<br/>                                                                                                                                          |
| [**IsOwnerClearDisabled**](isownercleardisabled-win32-tpm.md)                           | Indica se o proprietário do TPM pode limpar o TPM.<br/>                                                                                                                               |
| [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)                               | Indica se um proprietário do TPM pode ser instalado.<br/>                                                                                                                                  |
| [**IsPhysicalClearDisabled**](isphysicalcleardisabled-win32-tpm.md)                     | Indica se uma operação de presença física de TPM pode limpar o TPM.<br/>                                                                                                           |
| [**IsPhysicalPresenceHardwareEnabled**](isphysicalpresencehardwareenabled-win32-tpm.md) | Indica se este computador dá suporte a um caminho de hardware dedicado para sinalizar a presença física.<br/>                                                                                  |
| [**IsSrkAuthCompatible**](issrkauthcompatible-win32-tpm.md)                             | Indica se a autorização da chave de raiz de armazenamento (SRK) é compatível com o Windows.<br/>                                                                                           |
| [**RemoveBlockedCommand**](removeblockedcommand-win32-tpm.md)                           | Remove um comando TPM da lista local de comandos bloqueados pelo Windows.<br/>                                                                                                        |
| [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)                                   | Redefine o período de tempo limite ou outro mecanismo que os fabricantes de TPM implementam para proteger contra ataques de dicionário no TPM.<br/>                                                 |
| [**ResetSrkAuth**](resetsrkauth-win32-tpm.md)                                           | Redefine o valor de autorização da chave raiz de armazenamento (SRK) para ser compatível com o Windows.<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | Executa um teste automático do TPM e retorna o resultado.<br/>                                                                                                                          |
| [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)               | Solicita a execução de uma operação de presença física do TPM.<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | Instala um proprietário para o TPM.<br/>                                                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TPM** tem essas propriedades.

<dl> <dt>

**Inicial de isActivated \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o TPM está ativado.

**true** se o dispositivo estiver ativado (ou seja, se **isActivated \_ InitialValue** for true); caso contrário, **false**.

Esse valor é armazenado quando a classe é instanciada. É possível que o TPM altere o estado entre a instanciação e quando você marca esse valor. Para verificar se o TPM está ativado em tempo real, use o método [**isActivated**](isactivated-win32-tpm.md) .

**Windows Server 2008 e Windows Vista:** Esta propriedade não está disponível.

</dd> <dt>

**Inicial de IsEnabled \_**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o TPM está habilitado.

**true** se o dispositivo estiver habilitado (ou seja, se **IsEnabled \_ inicialvalue** for true); caso contrário, **false**.

Esse valor é armazenado quando a classe é instanciada. É possível que o TPM altere o estado entre a instanciação e quando você marca esse valor. Para verificar se o TPM está habilitado em tempo real, use o método [**IsEnabled**](isenabled-win32-tpm.md) .

**Windows Server 2008 e Windows Vista:** Esta propriedade não está disponível.

</dd> <dt>

**\_Inicialvalue de propriedade**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o TPM tem um proprietário.

**true** se o dispositivo tiver um proprietário (ou seja, se isdelede **\_ inicial** for true); caso contrário, **false**.

Esse valor é armazenado quando a classe é instanciada. É possível que o TPM altere o estado entre a instanciação e quando você marca esse valor. Para verificar se o TPM pertence ao tempo real, [**use o método**](isowned-win32-tpm.md) IsDeleted.

**Windows Server 2008 e Windows Vista:** Esta propriedade não está disponível.

</dd> <dt>

**ManufacturerID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As informações de identificação que nomeiam exclusivamente o fabricante do TPM.

Quando os dados estiverem indisponíveis, zero será retornado.

Esse valor inteiro pode ser convertido em um valor de cadeia de caracteres interpretando cada byte como um caractere ASCII. Por exemplo, um valor inteiro de 1414548736 pode ser dividido nesses 4 bytes: 0x54, 0x50, 0x4D e 0x00. Supondo que a cadeia de caracteres seja interpretada da esquerda para a direita, esse valor inteiro é convertido em um valor de cadeia de caracteres "TPM".

</dd> <dt>

**ManufacturerVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão do TPM, conforme especificado pelo fabricante.

Quando os dados não estão disponíveis, "sem suporte" é retornado.

</dd> <dt>

**ManufacturerVersionInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Outras informações de versão específicas do fabricante para o TPM.

Quando os dados não estão disponíveis, "sem suporte" é retornado.

</dd> <dt>

**PhysicalPresenceVersionInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão da interface de presença física, um mecanismo de comunicação usado para executar operações de dispositivo que exigem a presença física, à qual o computador dá suporte.

Essa interface deve estar disponível para executar operações de presença física do TPM. Os métodos do **\_ TPM do Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)e [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expõem os recursos da interface de presença física.

Quando os dados não estão disponíveis, "sem suporte" é retornado.

</dd> <dt>

**SpecVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão da especificação de Trusted Computing Group (TCG) à qual o TPM dá suporte. Esse valor inclui a versão de especificação de TCG principal e secundária, o nível de revisão de especificação e o nível de revisão de errata. Todos os valores estão em hexadecimal. Por exemplo, uma informação de versão de "1,2, 2, 0" indica que o dispositivo foi implementado para a especificação de TCG versão 1,2, nível de revisão 2 e sem errata.

Quando os dados não estão disponíveis, "sem suporte" é retornado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



 

 
