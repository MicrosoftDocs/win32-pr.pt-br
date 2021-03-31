---
title: Chaves do registro COM
description: Chaves do registro COM
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b85bb84b0a6f2e6ccc233b68af2889f4cb11ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822682"
---
# <a name="com-registry-keys"></a>Chaves do registro COM

O registro contém uma infinidade de informações usadas pelo COM. As informações mais importantes são armazenadas nas chaves a seguir.



| Chave                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Agrupa as opções de configuração (um conjunto de valores nomeados) para um ou mais objetos COM distribuídos em um único local no registro. As subchaves sob essa chave são usadas para mapear um identificador de aplicativo (AppID) para um nome de servidor remoto. Para simplificar o gerenciamento de configurações comuns de segurança e de configuração, os objetos COM distribuídos hospedados pelo mesmo executável são agrupados em uma AppID.<br/>                                                                                                                                                                                                                                                                                                                      |
| [CLSID](clsid-key-hklm.md)<br/>                              | Um identificador de classe (CLSID) é um identificador global exclusivo que identifica um objeto de classe COM. Se o servidor ou o contêiner permitir a vinculação a objetos incorporados, registre um CLSID para cada classe de objetos com suporte. A chave CLSID contém informações usadas pelo manipulador COM padrão para retornar informações sobre uma classe quando ela estiver no estado executando.<br/> Para obter um CLSID para seu aplicativo, use uuidgen.exe, encontrado no \\ diretório de ferramentas do kit de ferramentas com ou use [**falha em CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Um ProgID (identificador programático) é uma entrada de registro que pode ser associada a um CLSID. A chave ProgID mapeia uma cadeia de caracteres amigável para o usuário para um CLSID. Assim como o CLSID, o ProgID identifica uma classe, mas com menos precisão. Use uma ProgID em situações de programação em que não é possível usar um CLSID. ProgIDs não devem aparecer na interface do usuário. Não há garantia de que os ProgIDs sejam exclusivos, portanto, eles podem ser usados somente quando as colisões de nome não ocorrem.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Associa um ProgID a um CLSID. Ele é usado para determinar a versão mais recente de um aplicativo de objeto. Como o ProgID, o ProgID independente de versão pode ser registrado com um nome legível. <br/> Os aplicativos devem registrar um identificador programático independente de versão na chave VersionIndependentProgID. O ProgID independente de versão refere-se à classe do aplicativo e não muda de versão para versão, em vez de constante restante em todas as versões. Ele é usado com linguagens de macro e refere-se à versão atualmente instalada da classe do aplicativo. O ProgID independente de versão deve corresponder ao nome da versão mais recente do aplicativo de objeto. <br/> |
| [extensão de arquivo \_](-file-extension--key.md)<br/>              | Associa uma extensão de nome de arquivo a um ProgID.<br/> As informações contidas na chave de extensão de nome de arquivo são usadas pelos [monikers](file-monikers.md)System e File. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa a chave de extensão de nome de arquivo para fornecer o CLSID associado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interface](interface-key.md)<br/>                           | Registra novas interfaces associando um nome de interface a um IID (identificador de interface). Ele mapeia IIDs para informações específicas de uma interface. As informações são necessárias principalmente para usar interfaces entre limites de processo. <br/> Ao adicionar uma nova interface, a chave de interface deve ser concluída para COM para registrar a nova interface. Deve haver uma subchave IID para cada nova interface. <br/>                                                                                                                                                                                                                                                                                                       |
| [OleDb](hkey-local-machine-software-microsoft-ole.md)<br/>     | Controla as permissões de inicialização e acesso padrão para objetos COM distribuídos, bem como recursos de segurança em nível de chamada para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Somente os administradores têm acesso completo a essa parte do registro. Todos os outros usuários têm acesso somente leitura. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 





