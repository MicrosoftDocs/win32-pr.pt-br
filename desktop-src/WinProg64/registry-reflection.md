---
title: Reflexão do registro
description: O redirecionador de registro isola os aplicativos de 32 bits e 64 bits fornecendo exibições lógicas separadas de determinadas partes do registro no WOW64. No entanto, os valores de algumas chaves do registro devem ser os mesmos nas exibições de 32 bits e 64 bits.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- reflexão de registro 64-bit Windows programação
- reflexão 64-bit Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9104ba6bf4d537a597a2a45bfd9034379ed1781dd893e23633c08e9e9c1149b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899036"
---
# <a name="registry-reflection"></a>Reflexão do registro

\[as informações neste tópico se aplicam ao Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP. a partir do Windows 7 e do Windows Server 2008 R2, o WOW64 não usa mais a reflexão do registro e, anteriormente, as chaves refletidas são compartilhadas. Para obter mais informações, consulte [chaves do registro afetadas pelo WOW64](shared-registry-keys.md).\]

O [redirecionador de registro](registry-redirector.md) isola os aplicativos de 32 bits e 64 bits fornecendo exibições lógicas separadas de determinadas partes do registro no WOW64. No entanto, os valores de algumas chaves do registro devem ser os mesmos nas exibições de 32 bits e 64 bits.

O processo de *reflexão do registro* copia chaves e valores do registro entre duas exibições do registro para mantê-las sincronizadas. Cada exibição tem uma cópia física separada de cada chave do registro refletida, uma para a exibição do registro de 32 bits e a outra para a exibição do registro de 64 bits.

Uma chave refletida é copiada quando uma chave é fechada chamando [**falha RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey). Observe que isso oferece aumento para uma possível condição de corrida: se mais de um processo alterar a chave refletida, a última chamada **falha RegCloseKey** determinará o valor final da chave.

O refletor copia dados de ativação COM para servidores locais entre os modos de exibição, mas não copia dados em processo porque a combinação de dados em processo 32/64 não é permitida em Windows de 64 bits.

A reflexão não está habilitada para chaves de registro compartilhadas ou para chaves do registro que não são redirecionadas. Por exemplo, a reflexão não está habilitada para a chave do **\_ \_ \\ sistema do computador local hKey** . Para obter uma lista de chaves do registro redirecionadas, compartilhadas ou refletidas, consulte [chaves do registro afetadas pelo WOW64](shared-registry-keys.md).

A reflexão do registro usa uma política "último escritor vence", conforme ilustrado no exemplo a seguir:

-   após uma instalação limpa do Windows de 64 bits, o Wordpad.exe de 64 bits é registrado para lidar com os arquivos .doc. O refletor copia o registro de .doc da exibição do registro de 64 bits para a exibição do registro de 32 bits.
-   um administrador instala o Office de 32 bits, que registra Winword.exe de 32 bits para manipular .doc arquivos na exibição de registro de 32 bits. O refletor de registro copia essas informações na exibição do registro de 64 bits, de modo que os aplicativos de 32 bits e de 64 bits iniciem a versão de 32 bits do Winword.exe para arquivos de .doc.
-   um administrador instala o Office de 64 bits, que registra Winword.exe de 64 bits para manipular .doc arquivos na exibição de registro de 64 bits. O refletor de registro copia essas informações no registro de 32 bits, de modo que os aplicativos de 32 bits e de 64 bits iniciem a versão de 64 bits do Winword.exe para arquivos de .doc.

Portanto, as informações de associação de arquivo são preservadas para o aplicativo instalado mais recentemente.

Ele pode ser útil para aplicativos de 32 bits e 64 bits para compartilhar valores de chave de registro específicos que são normalmente gravados em exibições de registro separadas. Por exemplo, um servidor OLE de 32 bits que pode atender a solicitações de clientes de 32 bits e 64 bits pode disponibilizar seus dados de registro de 32 bits para a exibição de 64 bits do registro do sistema.

Quando um componente grava dados no registro do sistema, o WOW64 analisa as informações e faz uma cópia dos dados na exibição alternativa do registro quando apropriado. Normalmente, esse processo mantém duas cópias físicas separadas das mesmas chaves do registro em ambas as exibições no registro e é chamada de reflexo do registro ou espelhamento do registro.

A maioria das chaves sob a raiz de classes está nessa categoria. As atualizações para as chaves são refletidas quando a atualização é concluída e o identificador para a chave é fechado. Em casos específicos, as gravações em uma chave não serão refletidas se a chave tiver alguma dependência de bit de bits. Por exemplo, a chave InprocServer32 de 32 bits não é relevante para aplicativos de 64 bits, portanto, a chave InprocServer32 não é refletida na exibição do registro de 64 bits. No entanto, os aplicativos de 64 bits podem usar a chave LocalServer32 de 32 bits e a chave LocalServer32 é refletida.

Para **HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID** e **HKEY \_ Current \_ user \\ software \\ classes \\ CLSID**, somente os CLSIDs que não especificam InprocServer32 ou InprocHandler32 são refletidos. Somente os CLSIDs LocalServer32 são refletidos porque são executados fora do processo e podem ser ativados por aplicativos de 32 ou 64 bits. Os CLSIDs InProcServer32 não são refletidos porque não é possível carregar uma DLL de 32 bits para execução em um processo de 64 bits ou uma DLL de 64 bits para execução em um processo de 32 bits.

Para **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID** e **HKEY \_ Current \_ user \\ software \\ classes \\ AppID**, os valores de registro [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) não serão refletidos se seu valor for uma cadeia de caracteres vazia.

Para desabilitar e habilitar a reflexão do registro para uma determinada chave refletida, use as funções [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) . Essas funções não afetam as chaves que não estão na lista de chaves refletidas anteriormente neste tópico. Os aplicativos devem desabilitar a reflexão somente para as chaves do registro que elas criam e não tentar desabilitar a reflexão para as chaves predefinidas, como **HKEY \_ local \_ Machine** ou **HKEY \_ Current \_ User**. Para determinar se as chaves na lista de reflexão foram desabilitadas, use a função [**RegQueryReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey) .

As chaves refletidas não devem ser usadas em operações de registro transacionadas. Gravar em chaves refletidas durante uma transação pode fazer com que a transação falhe. Para obter mais informações sobre transações, consulte [kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Redirecionador de registro](registry-redirector.md)
</dt> <dt>

[Reflexão do registro no Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Chaves do Registro afetadas pelo WOW64](shared-registry-keys.md)
</dt> </dl>

 

 