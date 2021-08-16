---
description: A tabela SelfReg contém informações sobre módulos que precisam ser auto-registrados.
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

A tabela SelfReg contém informações sobre módulos que precisam ser auto-registrados. O instalador chama a [**função DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante a instalação do módulo; ele chama [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durante a desinstalação do módulo. O instalador não registra arquivos EXE por conta própria.

A tabela SelfReg tem as seguintes colunas.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Arquivo\_ | [Identificador](identifier.md) | Y   | N        |
| Custo   | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Arquivo\_
</dt> <dd>

Chave externa na primeira coluna da tabela [Arquivo indicando](file-table.md) o módulo que precisa ser registrado.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Custo
</dt> <dd>

O custo de registrar o módulo em bytes. Esse deve ser um número não negativo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os autores do pacote de instalação são fortemente aconselhados a usar o autoregiso. Em vez disso, eles devem registrar módulos por meio da e autor de uma ou mais tabelas fornecidas pelo instalador para essa finalidade. Para obter mais informações, consulte [Grupo de Tabelas do Registro](registry-tables-group.md). Muitos dos benefícios de ter um serviço de instalador central são perdidos com o autoregiso porque as rotinas de autoregisão tendem a ocultar informações críticas de configuração. Os motivos para evitar o autoregiso incluem:

-   A replicação de uma instalação com módulos auto-registrados não pode ser feita com segurança usando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) porque não há nenhuma maneira de dizer se as chaves auto-registradas são usadas por outro recurso ou aplicativo.
-   A capacidade de usar o anúncio será reduzida se o registro do servidor de classe ou extensão for executado dentro de rotinas de autoregisão.
-   O instalador trata automaticamente as chaves HKCR nas tabelas do Registro para instalações por usuário ou por computador. [**As rotinas DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) atualmente não suportam a noção de uma chave HKCR por usuário.
-   Se vários usuários estão usando um aplicativo auto-registrado no mesmo computador, cada usuário deve instalar o aplicativo na primeira vez que o executar. Caso contrário, o instalador não poderá determinar facilmente que as chaves de registro HKCU apropriadas existam.
-   O [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) poderá ter o acesso negado aos recursos de rede, como bibliotecas de tipo, se um componente for especificado como run-from-source e estiver listado na tabela SelfReg. Isso pode fazer com que a instalação do componente falhe durante uma instalação administrativa.
-   DLLs de auto-registro são mais suscetíveis a erros de codificação porque o novo código necessário para [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) é normalmente diferente para cada DLL. Em vez disso, use as tabelas do Registro no banco de dados para aproveitar o código existente fornecido pelo instalador.
-   As DLLs de auto-registro às vezes podem ser vinculadas a DLLs auxiliares que não estão presentes ou são a versão errada. Por outro lado, o instalador pode registrar as DLLs usando as tabelas do Registro sem dependência no estado atual do sistema.

> [!Note]  
> Você não pode especificar a ordem na qual o instalador registra ou registra as DLLs de auto-registro usando as ações [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules.](selfunregmodules-action.md) Consulte [Especificando a ordem de auto-registro.](specifying-the-order-of-self-registration.md)

 

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
