---
description: A tabela a seguir descreve \_ as opções sol de soquete do AppleTalk que se aplicam aos soquetes criados para a família de endereços AppleTalk (AF \_ AppleTalk).
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: Opções de soquete SOL_APPLETALK (Atalkwsh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SOL_APPLETALK
- Windows
api_type:
- HeaderDef
api_location:
- Atalkwsh.h
ms.openlocfilehash: 146cfa02706cc9a2669cf21ba6d9eac0ac74ee4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764158"
---
# <a name="sol_appletalk-socket-options"></a>Opções de soquete de SOL \_

A tabela a seguir descreve as opções sol de soquete do **\_ AppleTalk** que se aplicam aos soquetes criados para a família de endereços AppleTalk (AF \_ AppleTalk). Consulte as páginas de referência de função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**Opções de soquete de SOL \_**</dt> <dd> <dl> <dt> 

| Opção                          | Obter | Definir | Tipo de optval                          | Descrição                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Portanto, \_ confirme o \_ nome               | sim |     | **\_tupla de NBP do WSH \_**                  | Confirma que um determinado nome AppleTalk está associado ao endereço fornecido.                                                                                                                                  |
| Então, \_ DESREGISTRE o \_ nome            |     | sim | **\_nome do registro do WSH \_**              | Cancela o registro do nome da rede.                                                                                                                                                               |
| \_GETLOCALZONES               | sim |     | **\_zonas de pesquisa do WSH \_**               | Retorna uma lista de nomes de zona conhecida pelo nome de adaptador fornecido.                                                                                                                                        |
| \_GETMYZONE                   | sim |     | º \[\]                            | Retorna a zona padrão na rede.                                                                                                                                                             |
| \_GETNETINFO                  | sim |     | **o WSH \_ pesquisa \_ NETDEF \_ no \_ adaptador** | Retorna os valores propagados para a rede, bem como a zona padrão. O parâmetro *optlen* deve ser pelo menos um byte maior do que o tamanho da **consulta do WSH \_ \_ na estrutura \_ do \_ adaptador** .  |
| Então \_ GETzonelist                 | sim |     | **\_zonas de pesquisa do WSH \_**               | Retorna nomes de zona da lista de zona da Internet. O parâmetro *optlen* deve ser pelo menos um byte maior que o tamanho da estrutura **de \_ \_ zonas de pesquisa do WSH** .                                       |
| Portanto, \_ pesquise \_ MyZone              | sim |     |                                      | O mesmo que \_ GETMYZONE                                                                                                                                                                                |
| Então \_ , \_ nome da pesquisa                | sim |     | **\_nome de pesquisa do WSH \_**                | Pesquisa um nome de NBP especificado e retorna as tuplas correspondentes de informações de nome e NBP. O parâmetro *optlen* deve ser pelo menos um byte maior que o tamanho da estrutura do \_ nome de pesquisa do WSH \_ . |
| Então, \_ pesquise o \_ NETDEF \_ no \_ adaptador | sim |     | **o WSH \_ pesquisa \_ NETDEF \_ no \_ adaptador** | O mesmo que \_ GETNETINFO.                                                                                                                                                                              |
| Portanto \_ , \_ zonas de pesquisa               | sim |     | **\_zonas de pesquisa do WSH \_**               | O mesmo que \_ GETzonelist.                                                                                                                                                                             |
| Portanto \_ , \_ zonas \_ de pesquisa no \_ adaptador  | sim |     | **\_zonas de pesquisa do WSH \_**               | O mesmo que \_ GETLOCALZONES.                                                                                                                                                                           |
| Portanto, o \_ PAP \_ Obtém o \_ status do servidor \_    | sim |     | **\_ \_ \_ status do servidor Get PAP do WSH \_**    | Retorna o status do PAP de um determinado servidor                                                                                                                                                           |
| Portanto \_ , \_ Leia a linha PAP \_            |     | sim | º \[\]                            | Essa chamada Prime uma leitura em uma conexão PAP para que o remetente possa começar a enviar os dados                                                                                                                 |
| Portanto \_ , \_ defina o \_ status do servidor do PAP \_    |     | sim | º \[\]                            | Define o status a ser enviado se outro cliente solicitar o status                                                                                                                                     |
| Portanto \_ , \_ nome do registro              |     | sim | **\_nome do registro do WSH \_**              | Registra o nome fornecido na rede AppleTalk                                                                                                                                                    |
| Então, \_ Remover \_ nome                |     | sim | **\_nome do registro do WSH \_**              | O mesmo que \_ o nome de CANcelamento de registro \_                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Suporte do Windows para opções de SOL do \_ APPLETALK**</dt> <dd> <dl> <dt> 

| Opção                          | Windows Vista e posterior | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| Portanto, \_ confirme o \_ nome               |                         | x                   | x          | x            | x           |               |
| Então, \_ DESREGISTRE o \_ nome            |                         | x                   | x          | x            | x           |               |
| \_GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| \_GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| \_GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| Então \_ GETzonelist                 |                         | x                   | x          | x            | x           |               |
| Portanto, \_ pesquise \_ MyZone              |                         | x                   | x          | x            | x           |               |
| Então \_ , \_ nome da pesquisa                |                         | x                   | x          | x            | x           |               |
| Então, \_ pesquise o \_ NETDEF \_ no \_ adaptador |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ zonas de pesquisa               |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ zonas \_ de pesquisa no \_ adaptador  |                         | x                   | x          | x            | x           |               |
| Portanto, o \_ PAP \_ Obtém o \_ status do servidor \_    |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ Leia a linha PAP \_            |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ defina o \_ status do servidor do PAP \_    |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ nome do registro              |                         | x                   | x          | x            | x           |               |
| Então, \_ Remover \_ nome                |                         | x                   | x          | x            | x           |               |



 

As opções de **sol \_ APPLETALK** só têm suporte nas versões de servidor do Windows 2000 e do Windows NT 4,0.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

As opções de soquetes do sol e as estruturas usadas por essas opções de soquete são definidas no arquivo de cabeçalho *Atalkwsh. h* . **\_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Atalkwsh. h</dt> </dl> |



 

 




