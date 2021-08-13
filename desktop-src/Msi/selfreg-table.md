---
description: A tabela SelfReg contém informações sobre os módulos que precisam ser registrados automaticamente.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabela SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d00b9f18755cf3284edfd1ba9476b12ba6343c816dbafe84ac3c3676f663f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625502"
---
# <a name="selfreg-table"></a>Tabela SelfReg

A tabela SelfReg contém informações sobre os módulos que precisam ser registrados automaticamente. O instalador chama a função [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante a instalação do módulo; Ele chama [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durante a desinstalação do módulo. O instalador não registra automaticamente arquivos EXE.

A tabela SelfReg tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Grupo\_ | [Identificador](identifier.md) | Y   | N        |
| Cost   | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [arquivos](file-table.md) que indica o módulo que precisa ser registrado.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Custo
</dt> <dd>

O custo de registrar o módulo em bytes. Este deve ser um número não negativo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os autores do pacote de instalação são altamente aconselhados em relação ao uso de auto-registro. Em vez disso, eles devem registrar módulos criando uma ou mais tabelas fornecidas pelo instalador para essa finalidade. Para obter mais informações, consulte [grupo de tabelas do registro](registry-tables-group.md). Muitos dos benefícios de ter um serviço do instalador central são perdidos com o auto-registro porque as rotinas de Autoregistro tendem a ocultar informações de configuração críticas. Os motivos para evitar o auto-registro incluem:

-   A reversão de uma instalação com módulos autoregistrados não pode ser feita com segurança usando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) porque não há nenhuma maneira de informar se as chaves autoregistradas são usadas por outro recurso ou aplicativo.
-   A capacidade de usar o anúncio será reduzida se o registro do servidor de extensão ou de classe for executado em rotinas de auto-registro.
-   O instalador manipula automaticamente as chaves de HKCR nas tabelas do registro para instalações por usuário ou por computador. Atualmente, as rotinas de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) não dão suporte à noção de uma chave de HKCR por usuário.
-   Se vários usuários estiverem usando um aplicativo AutoRegistrado no mesmo computador, cada usuário deverá instalar o aplicativo na primeira vez que executá-lo. Caso contrário, o instalador não poderá determinar facilmente que as chaves de Registro HKCU apropriadas existam.
-   A [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) pode ter acesso negado a recursos de rede, como bibliotecas de tipos, se um componente for especificado como Run-from-Source e estiver listado na tabela selfreg. Isso pode fazer com que a instalação do componente falhe durante uma instalação administrativa.
-   As DLLs de registro automático são mais suscetíveis a erros de codificação porque o novo código necessário para [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) é normalmente diferente para cada DLL. Em vez disso, use as tabelas do registro no banco de dados para aproveitar o código existente fornecido pelo instalador.
-   As DLLs de registro automático podem, às vezes, se vincular a DLLs auxiliares que não estão presentes ou estão na versão errada. Por outro lado, o instalador pode registrar as DLLs usando as tabelas do registro sem dependência no estado atual do sistema.

> [!Note]  
> Não é possível especificar a ordem na qual o instalador registra ou cancela o registro de DLLs de Autoregistro usando as ações [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) . Consulte [especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md).

 

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
